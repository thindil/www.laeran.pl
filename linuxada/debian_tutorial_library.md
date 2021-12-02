-- layout: default
-- title: Creating Debian package for a library
**Important:** This tutorial is about creating Debian package for Ada Linux
Packages Repository, not the official Debian packages. It uses greatly
simplified way to create a package which will be not follow Debian Package
guidelines or even guidelines for Ada packages for Debian. It may change over
time. Also, this tutorial is in early stage of work. If you have any questions
or ideas about it, feel free to [contact with me](../contact.html). Below you
will find the list of changes to the document.

### History

* 01.12.2021 - Created

### Preparations

Before start creating a package, it is a good idea to prepare your workshop.
The best option is to work inside a Docker container. It will allow you to
keep your system clean, but also will be easier to find all required packages
to build the project. As the example here, I will use, an existing package
[tashy](https://build.opensuse.org/package/show/home:thindil/libtashy).

The most important thing needed to create a package is of course its content.
In this situation it will be an archive file with the source code of the future
package. Now one important note: Debian has requirement how that file and its
content should be named:

1. The archive file must be type *tar* compressed with *gzip*, extension
   *tar.gz*.
2. The file name must be *name-version.tar.gz*. In our example I use
   tashy program in version 8.6.12, thus the name of the file will be
   *tashy-8.6.12.tar.gz*.
3. Inside the archive file, the content of the source code, must be in
   directory *name-version*. Thus, in our example, the whole source code will be
   in directory *tashy-8.6.12*.

During the tutorial, to make things easier we will be using a few Debian
Package Maintainer tools, which should be installed inside the Docker image.
Exactly two programs: `debmake` and `debuild` and their dependencies. It is a
good idea to create a Docker image with them, because they will always be
needed, no matter what package we create.

You will also need any text editor. Some of them have even syntax highlighting
for Debian packages files. We will be using NeoVim for that.

If you use a Docker image to create the package, please install also all packages
required for build your package. In our example it will be:

    apt install -y gnat gprbuild tcl-dev tk-dev libfontconfig-dev

### Creating template Debian package

The first we start with creating empty Debian package with the default settings.
Unpack your library source code to the same directory where the archive file
is. In our example it will be:

    tar -xf tashy-8.6.12.tar.gz

Next, would be good to start our Docker image. :) It can look in that way
(replace the name of image (*ubuntu:21.10*) with your Image name):

    sudo docker run --rm -it -v $(pwd):/app -w /app ubuntu:21.10 /bin/bash

Enter the uncompressed directory and create the template directory for the
package:

    cd tashy-8.6.12
    debmake

And that's all, now it is time to set basic information about our package.

### Setting the package control file

The command `debmake` created a new directory in our source code directory,
called *debian*. It contains all needed files to create a Debian package. This
tutorial will not explain everything. If you want more information, please go
to proper Debian [wiki page](https://wiki.debian.org/Packaging).

Now we enter the *debian* directory and start editing the file *control*:

    cd debian
    nvim control

We start with changing *Section* of the package. It is important, because if we
don't do it, the package will not build. All available options are listed
[here](https://www.debian.org/doc/debian-policy/ch-archive.html#s-subsections).
In our example we set it to *libs*

    Section: libs

Next, the *Maintainer* field. It should have value `Your Name
<your@email.com>`

    Maintainer: Bartek thindil Jasicki <thindil@laeran.pl>

The next field is the most important and sometimes the hardest to fill:
*Build-Depends*. It contains names of all Debian packages needed for build our
package. It can be listed in one line, but it is more convenient to have each
package in a separated line. **Important:** always include the default line,
don't remove it. In our example we need packages with default versions: `gnat`,
`gprbuild`, `tcl-dev`, `tk-dev`, `libfontconfig-dev` and
`dh-sequence-ada-library`.

    Build-Depends: debhelper-compat (= 12),
     gprbuild,
     gnat,
     tcl-dev,
     tk-dev,
     libfontconfig-dev,
     dh-sequence-ada-library

**Notice:** Each new line should start with one space. This informs the build
system that it is continuation of the previous line. The last comma is simply
ignored.
The next field to change is *Homepage*. Enter here your main project page
address:

    Homepage: https://www.laeran.pl/repositories/tashy/home

We have been creating three Debian packages: library itself, the development files
for the library and documentation package. Let's start with the development
package.

The first, we set the name of the development package, in our example it will
be *libtashy-dev*. All development libraries should have name starting with
*lib* prefix and ending with *-dev* suffix.

    Package: libtashy-dev

Our development package requires other packages to run, mostly to simplify
build the development tools chain (like compiler, etc.). It is a good idea to
list them in the *Depends* field. In our example it will be look that:

    Depends: ${misc:Depends},
     ${ada:Depends},
     tcl-dev,
     tk-dev,
     libfontconfig-dev

Generally, the content of the *Depends* field for development packages of
libraries is very similar to field *Build-Depends*.

Also, it would be good if our development package also recommends the
development documentation package of our library (the package which we will
create later). It is done by adding field *Suggest*:

    Suggests: libtashy-doc

The last thing is to add the description of our development package. Usually,
the description is made from two parts. The first part is the default
description of the library, the second part is short sentence that this is a
development package.

    Description: TASHY is short from Tcl Ada SHell Younger.
     It is derivate of TASH. It allow to use Tcl code in an Ada
     code and vice versa.
     .
     Install this package if you want to write programs that use
     TASHY.

**Notice:** If you want to make two paragraphs in the description, use line
with dot only between them, like in our example.

**Notice:** Also here, each new line should start with one space. This informs
the build system that it is continuation of the previous line.

The second package will be the library itself. Again, the name of the package
should start wit *lib* prefix, in our example *libtashy*.

    Package: libtashy

The same as with the development version, our package needs to run a few
others. We have to list all of them in *Depends* field.

    Depends: ${misc:Depends},
     ${shlibs:Depends},
     tcl,
     tk,
     tklib

And as above, add the description of our package.

    Description: TASHY is short from Tcl Ada SHell Younger.
     It is derivate of TASH. It allow to use Tcl code in an Ada
     code and vice versa.

The last package build from our project is the package with the documentation.
In our example it is a development documentation. This same which
*libtashy-dev* suggest. Thus, again we define package name. The name must
starts with *lib* prefix and ends with *-doc* suffix. Our package will be named
*libtashy-doc*.

    Package: libtashy-doc

The documentation package must have assigned a different section: *doc*. To set
it for our package we add field *Section*.

    Section: doc

The next step says that our package is platform-independent. After all, our
documentation is a set of HTML files. Thus, we set the field *Architecture* and
the field *Multi-Arch*:

    Architecture: all
    Multi-Arch: foreign

Our documentation doesn't depend on any particular package, so let's set the
*Depends* field to the default value.

    Depends: ${misc:Depends}

Optionally, we suggest the Ada compiler. You don't need to do it in your
package.

    Suggests: gnat

And as last, again, set the description for the documentation package:

    Description: TASHY is short from Tcl Ada SHell Younger.
     It is derivate of TASH. It allow to use Tcl code in an Ada
     code and vice versa.
     .
     This package contains the documentation.

Now, save the **control** file and let's move to the next. More information
about the fields in the file you can find [here](https://www.debian.org/doc/debian-policy/ch-controlfields.html).

### Setting the package rules file

Now we start editing the file *rules*

    nvim rules

Generally, this file is standard GNU Makefile. It contains commands which will
be executed during creating the package, like configuring, build and installing
the files. At the start it is a good idea to remove all unneeded comments from
the start of the file as the comment there suggest. After that we can start
modifying it to our needs. **IMPORTANT:** use only Tab in that file for
indentation. In other case it will **not works**. The build program will
report invalid file. If the example contains spaces, you will have to manually
convert them to tabs. This is the reason why it is better to use a text editor
with support for Debian packages (like Vim or Emacs). They automatically change
all indentation in *rules* file into tabs. In the examples here, spaces are
used, thus if you copy and paste them to your *rules* file you will have to
convert them to tabs.

The first, we overwrite the default build action. Because our package uses
gprbuild with custom variables, we have to set our own build command. Also, our
package have to be configured before we can build it. Add at the end of the
file lines:

    override_dh_auto_build:
        scripts/setup.tcl --nogui
        gprbuild -P tashy.gpr -XLIBRARY_TYPE=static
        gprbuild -P tashy.gpr -XLIBRARY_TYPE=relocatable

The second thing, is to install our build binary in proper location. During
creation of a package, all files which later should be installed from the
package are located in *debian/packagename/* directory. In our example it will
be *debian/libtashy/* directory. Also, we need separated subdirectories
for each other package, in our example it will be *debian/libtashy-dev* and
*debian/libtashy-doc*. We have to create them, with a proper Linux directory
tree structure and then put our library, development files and documentation
there. Because we don't use for this standard `make install` command, we have
to override it, in the same way as we have done it with the build command.
Add at the end of the file lines:

    override_dh_auto_install:
        gprinstall -f -P tashy.gpr --create-missing-dirs -XLIBRARY_TYPE=static --build-var=LIBRARY_TYPE --build-name=static --prefix=$(CURDIR)/debian/libtashy/usr/
        gprinstall -f -P tashy.gpr --create-missing-dirs -XLIBRARY_TYPE=relocatable --build-var=LIBRARY_TYPE --build-name=relocatable --prefix=$(CURDIR)/debian/libtashy/usr/
        mkdir -p $(CURDIR)/debian/libtashy-dev/usr/share/
        mv $(CURDIR)/debian/libtashy/usr/include $(CURDIR)/debian/libtashy-dev/usr/
        cp -r $(CURDIR)/debian/libtashy/usr/lib $(CURDIR)/debian/libtashy-dev/usr/
        rm $(CURDIR)/debian/libtashy/usr/lib/tashy.relocatable/*.ali
        rm $(CURDIR)/debian/libtashy/usr/lib/tashy.static/*.ali
        rm $(CURDIR)/debian/libtashy-dev/usr/lib/tashy.relocatable/*.so
        rm $(CURDIR)/debian/libtashy-dev/usr/lib/*.so
        rm $(CURDIR)/debian/libtashy-dev/usr/lib/tashy.static/*.a
        mv $(CURDIR)/debian/libtashy/usr/share/gpr $(CURDIR)/debian/libtashy-dev/usr/share/
        mkdir -p $(CURDIR)/debian/libtashy-doc/usr/share/doc/libtashy-doc/
        cp -r $(CURDIR)/docs $(CURDIR)/debian/libtashy-doc/usr/share/doc/libtashy-doc/

That's all here. Save the file.

### Setting the changelog file

This is also important step during creating a package. The version number from
the *changelog* file is used to create versioning for the package. The version
number is in parentheses in the first line. In our example, it is *8.6.12-1*.
8.6.12 is official version of the program, 1 is the first release as Debian package.
When we will update the existing package of the same version, we should change
this number and add a new changelog entry for it. In our example we can change
word *UNRELEASED* (as a name for Debian version) to *impish* (the name of
the current Ubuntu version). This step is optional. Also, it is good idea to change
the entry of changelog to just:

    * Initial release

And update our contact information, automatically generated by `debmake`
command. Again, save the file. We finished setting our package. :)

### Build the package

If we set everything properly, and we gathered all needed prerequisites for the
package, the build process should be automatic and straightforward. In the main
directory of source code (outside *debian* directory) execute `debuild`
command. If you are still in *debian* directory it will look that:

    cd ..
    debuild -d

The parameter `-d` isn't needed, especially during the first try to build the
package. It instructs the build system that it is allowed to overwrite any
existing files like previously created *.deb* packages etc. If you build the
package inside container, there will be errors about lack of GPG key. Don't
worry about it, for Ada Linux Package Repository it is even better (look below
to the Notes section).

If everything is OK, our package now should be fully build. If not, please
check all the information which are appeared on the screen during the build
process to see what goes wrong. If the process finished successfully, you
should end with a few files. Here is the list of only needed files:

1. *packagename_version.debian.tar.gz* This file contains our *debian*
   directory with all changes which we have done to files there. In our example the
   file will be named *tashy_8.6.12-1.debian.tar.gz*
2. *packagename_version.dsc* This file contains checksums and base information
   about our package. In the example the name of the file is *tashy_8.6.12-1.dsc*.
3. Soft link *package_version.orig.tar.gz* which links to your source code
   archive file. In the example it is *tashy_8.6.12-1.orig.tar.gz*

There is also your newly created Debian package, thus you can test it now. :)
Any other files are not needed to create a new package. You can delete them.
There is also a good idea to rename our archive file to replace the link.
**Important:** pay attention that link uses underscore in the name instead of
dash:

    rm tashy_8.6.12-1.orig.tar.gz
    cp tashy-8.6.12.tar.gz tashy_8.6.12-1.orig.tar.gz

Now you can create your own repository at [Open SUSE Build Service](https://build.opensuse.org/)
and check if everything works there too. You will need to upload there all
three files. If everything is working, congratulation, you built your
first Debian package. :) To add the package to the Ada Linux Packages
Repository, use option *Submit package*.

### Notes

* If you build the package in your normal system, not in container, file
  *packagename_version.dsc* will be signed with your GPG key. Unfortunately,
  openSUSE Build Servive doesn't know your GPG key or even doesn't have
  installed the GPG during build a package, thus you need to remove
  signature from the file. Normally, it is a bad idea, but there is no
  other option. Open file *packagename_version.dsc*
  in your text editor and delete first three lines (up to Format line) and
  the last twelve lines (from the empty line after the last checksum).
* You can find all files related to the tutorial on the [libtashy](https://build.opensuse.org/package/show/home:thindil/tashy)
  package page.
