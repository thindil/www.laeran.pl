-- layout: default
-- title: Creating Debian package for a program
**Important:** This tutorial is about creating Debian package for Ada Linux
Packages Repository, not the official Debian packages. It uses greatly
simplified way to create a package which will be not follow Debian Package
guidelines or even guidelines for Ada packages for Debian. It may change over
time. Also, this tutorial is in early stage of work. If you have any questions
or ideas about it, feel free to [contact with me](../contact.html). Below you
will find the list of changes to the document.

### History

* 19.11.2021 - Created

### Preparations

Before start creating a package, it is a good idea to prepare your workshop.
The best option is to work inside of Docker container. It will allow you to
keep your system clean, but also will be easier to find all required packages
to build the project. As the example here, I will use, existing package
[bob](https://build.opensuse.org/package/show/home:thindil/bob).

The most important thing needed to create a package is of course its content.
In this situation it will be archive file with the source code of the future
package. Now one important note: Debian has requirement how that file and its
content should be named:

1. The archive file must be type *tar* compressed with *gzip*, extension
   *tar.gz*.
2. The file name must be *name-version.tar.gz*. In our example I use
   bob program in version 3.1, thus the name of the file will be
   *bob-3.1.tar.gz*.
3. Inside the archive file, the content of the source code, must be in
   directory *name-version*. Thus, in our example, the whole source code will be
   in directory *bob-3.1*.

During the tutorial, to make things easier we will be using a few Debian
Package Maintainer tools, which should be installed inside the Docker image.
Exactly two programs: `debmake` and `debuild`. It is good to create Docker
image with them, because they will always be needed, no matter what package we
create.

You will also need any text editor. Some of them have even syntax highlighting
for Debian packages files. We will be using NeoVim for that.

If you use Docker image to create the package, please install also all packages
required for build your package. In our example it will be:

    apt install -y gnat gprbuild

### Creating template Debian package

The first we start with creating empty Debian package with default settings.
Unpack your program source code to the same directory where the archive file
is. In our example it will be:

    tar -xf bob_3.1.tar.gz

Next, would be good to start our Docker image. :) It can look in that way
(replace the name of image with your Image name):

    sudo docker run --rm -it -v $(pwd):/app -w /app ubuntu:21.10 /bin/bash

Enter the uncompressed directory and create the template directory for the
package:

    cd bob-3.1
    debmake

And that's all, now it is time for set basic information about our package.

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
In our example we set it to *utils*

    Section: utils

Next, the *Maintainer* field. It should have value `Your Name
<your@email.com>`

    Maintainer: Bartek thindil Jasicki <thindil@laeran.pl>

The next field is the most important and sometimes the hardest to fill:
*Build-Depends*. It contains name of all Debian packages needed for build our
package. It can be listed in one line, but it is more convenient to have each
package in a separated line. **Important:** always include the default line,
don't remove it. In our example we need only two packages: `gnat` (default
version) and `gprbuild` (also default version).

    Build-Depends: debhelper-compat (= 12),
     gprbuild,
     gnat

The next field to change is *Homepage*. Enter here your main project page
address:

    Homepage: https://www.laeran.pl/repositories/bob/home

As our example doesn't need any additional packages to run, don't change
anything in *Depends* field. If your program depend on another package(s) you
will have to add them here in the same way as we modified *Build-Depends*
field.

The last thing to change in this file is to set field *Description* for the
package.

    Description: Bob is a Non-Intelligent console assistant. Bod
     doesn't try to replace any existing shells or build systems.
     It is designed to extend them. Often when you have few projects
     to work, they use different commands or build systems to maintain.
     To organize it, often you have to add or global aliases to your shell
     or create scripts which grow over time to maintain it. Bob trying to
     solve this problem by adding the ability to create local aliases for
     each directory. It is doing this by creating configuration files
     (in YAML) with defined aliases in each directory. When Bob is executed
     in a selected directory, it reads configuration file (if exists) for
     selected directory for aliases.

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
all indentation in *rules* file into tabs.

The first, we overwrite the default build action. Because our package uses
gprbuild with custom variables, we have to set our own build command. Add at
the end of the file lines:

    override_dh_auto_build:
        gprbuild -P bob.gpr -XMode=release

The second thing, is to install our build binary in proper location. During
creation of a package, all files which later should be installed from the
package are located in *debian/packagename/* directory. In our example it will
be *debian/bob/* directory. We have to create it, with proper Linux directory
tree structure and then put our binary there. Because we don't use for this
standard `make install` command, we have to override it in the same way as we
have done it with build command. Add at the end of the file lines:

    override_dh_auto_install:
        mkdir -p $(CURDIR)/debian/bob/usr/
        mv $(CURDIR)/bin $(CURDIR)/debian/bob/usr/

The last step is optional but useful. We override in it the default clean
action. It is used at start and end of build the package process. It can be
useful if we will rebuild the package again. To do it, add at the end of the
file lines:

    override_dh_auto_clean:
        gprclean -P bob.gpr

That's all here. Save the file.

### Setting the changelog file

This is also important step during creating a package. The version number from
the *changelog* file is used to create versioning for the package. The version
number is in parentheses in the first line. In our example, it is *3.1-1*. 3.1
is official version of the program, 1 is the first release as Debian package.
When we will update the existing package of the same version, we should change
this number and add new changelog entry for it. In our example we can change
word *UNRELEASED* (as a name for Debian version) to *impish* (the name of
current Ubuntu version). This step is optional. Also, it is good idea to change
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
   file will be named *bob_3.1-1.debian.tar.gz*
2. *packagename_version.dsc* This file contains checksums and base information
   about our package. In the example the name of the file is *bob_3.1-1.dsc*.
3. Soft link *package_version.orig.tar.gz* which links to your source code
   archive file. In the example it is *bob_3.1-1.orig.tar.gz*

There is also your newly created Debian package, thus you can test it now. :)
Any other files are not needed to create a new package. You can delete them.
There is also a good idea to rename our archive file to replace the link.
**Important:** pay attention that link uses underscore in the name instead of
dash:

    rm bob_3.1-1.orig.tar.gz
    cp bob-3.1.tar.gz bob_3.1-1.orig.tar.gz

Now you can create your own repository at [Open SUSE Build Service](https://build.opensuse.org/)
and check if everything works there too. You will need to upload there all
three files. If everything is working, congratulation, you built your
first Debian package. :)

### Notes

* If you build the package in your normal system, not in container, file
  *packagename_version.dsc* will be signed with your GPG key. Unfortunately,
  OBS doesn't know your GPG key or even doesn't have installed GPG during build
  a package, thus you need to remove signature from the file. Normally, it is a
  bad idea, but there is no other option. Open file *packagename_version.dsc*
  in your text editor and delete first three lines (up to Format line) and last
  12 lines (from the empty line after the last checksum).
* You can find all files related to the tutorial on the [bob](https://build.opensuse.org/package/show/home:thindil/bob)
  package page.
