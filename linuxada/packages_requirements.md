-- layout: default
-- title: Packages Requirements
-- summary: Information about initial conditions which package should meet to add it to the Ada Linux Packages Repository

The most requirements for packages are optional. The only mandatory rule is
the naming convention for packages which use the selected version of Ada
compiler. Each requirement has also included reason why it is here. If you
disagree with any of them or want to add something here, feel free to
[contact with me](../contact.html). This list can change from time to time,
thus before any submission, please look at it. Below you will find the list of
changes to the document.

### History

* 18.11.2021 - Created

### Naming convention:

1. The package's name can have any name you want. Of course, if a
   package with the same name exists in the repository, you will be asked
   for change it.

   Reason: It is technically impossible to have two or more packages with
   the same name. It also brings confusion to the users.

2. If the package requires exact version of Ada compiler, please append to
   its name the desired version of the compiler with leading dash. For
   example, if you want to add a package `gprbuild` which requires GNAT in
   version **11.x**, name your package `gprbuild-11`.

   Reason: A package which requires exact version of a compiler also
   often requires the whole set of libraries compiled with that compiler. If it
   delivers executable files, they can conflict with other executables built
   for different version of the compiler. The same problem can be with
   libraries, especially with development files.

3. Names and contents of the files used in creating the package, mostly
   these which contain source code of package, should follow Debian naming
   rules. For example, if you want to create package `gprbuild` with version
   *21*.1 the compressed file with the source code of package should be named
   `gprbuild_21.1.orig.tar.gz` and contains the source code in directory
   `gprbuild-21.1`.

   Reason: Debian packages probably as the only have requirements for naming
   convention of the source code files. Keeping with them will reduce the
   amount of work needed to create them. Also, it will remove double data from
   the repository.

### Testing packages

1. Before submit package to the repository, please create testing repository
   for yourself and check if everything is working as expected. Also, enable
   creation of binary packages.

   Reason: Before I will add the package to the repository, I want to be sure
   that it at least builds correctly. :) If you do this before submission, it
   will greatly speed up the process of adding the package to the repository.

2. Before submit a new version of package which you maintain into the
   repository also, please create a testing repository for yourself to check
   it.

   Reason: Probably the most of us don't like to have broken updates in our
   systems. This requirement also reduces the amount of work which will server
   have. And generally, keep the repository clean.

### Debian packages

1. It is recommended to overwrite default action `dh_auto_install` with own
   if you use `gprinstall` to install the package.

   Reason: The default installation for Ada creates very basic GNAT Project
   Configuration file (with extension `.gpr`). The modern version of
   `gprinstall` creates a lot better file, for example with possibility to
   select between static and relocatable version of the package.
