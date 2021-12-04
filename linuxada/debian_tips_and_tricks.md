-- layout: default
-- title: Tips and tricks for creating Debian packages
**Important:** This document showing various techniques used during creating
Debian packages for Ada Linux Packages Repository, not the official Debian
packages. It uses greatly simplified way to create a package which will
be not follow Debian Package guidelines or even guidelines for Ada packages
for Debian. It may change over time. Also, this document assumes that you have
read both tutorials about creating Debian packages for Ada Linux Packages
Repository. If you have any questions or ideas about it, feel free to
[contact with me](../contact.html). Below you will find the list of
changes to the document.

### History

* 03.12.2021 - Created

### Patches

From time to time it is necessary to patch the upstream source code in order
to compile it. Debian handles patch files in a bit of specific manner.

The first, create the patch file in normal way, for example with Git command
`git diff`. The command must be executed from the main directory of the
package, for example bob-3.1. Let's say we execute command `git diff >
mypatch.diff`

The second step. Put your patch file into *debian/patches* directory in the
package directory. Thus, again, if our package is *bob* version *3.1* the patch
should go to the directory *bob-3.1/debian/patches*. The terminal command in
our example will be, in the main directory, where we created the diff file: `mv
mypatch.diff debian/patches/`.

Inside the *debian/patches* directory there is the file *series*. Open it in
your favorite text editor. If this is a fresh file, remove any content from it
and add the name of the patch file.
If there are any patches added earlier, at the end of the file add your patch
name. In our example, because our patch is the first file, the whole *series*
file will look that:

    mypatch.diff

And that's all. Run as usual `debmake -d`. Your patch will be automatically
added to the source code of the package before it will be build.
