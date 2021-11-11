-- layout: default
-- title: Ada Linux Packages Repository
-- summary: Information about repository with Ada programming language related packages for various Linux distributions.

##### General information

[Ada Linux Packages Repository](https://build.opensuse.org/project/show/home:thindil)
contains various programs and libraries related to Ada programming language
for different Linux distributions. Not all the packages are available for
every distribution, same with various architectures. At this moment available
repositories are:

* Ubuntu 21.10 x86_64
* Debian 11 x86_64
* Debian Testing x86_64

To see the full list of available packages please go to the [repository page](https://build.opensuse.org/project/show/home:thindil).

##### Status

Current status of the project is [SNAFU](https://en.wikipedia.org/wiki/SNAFU).

There are several packages available, but they still need a lot of work,
especially to be conforming with [Debian policy for Ada](https://people.debian.org/~lbrenta/debian-ada-policy.html).
This mean that you should use them at your own risk. They **should** work but
they content and names can change from time to time. Any help in that matter is
very welcomed. :)

**WARNING:** The whole repository, same as this document is under construction
now thus, everything here is subject to change. Be ready for everything. :)

##### How to use it

First you have to add the repository to your repositories list. You can also
skip this step and download directly packages, but then you will not have
option to obtain automatically updates to them.

* For xUbuntu 21.10 run the following:

Keep in mind that the owner of the key may distribute updates, packages and
repositories that your system will trust ([more information](https://help.ubuntu.com/community/SecureApt)). In console enter:

   `echo 'deb http://download.opensuse.org/repositories/home:/thindil/xUbuntu_21.10/ /' | sudo tee /etc/apt/sources.list.d/home:thindil.list`

   `curl -fsSL https://download.opensuse.org/repositories/home:thindil/xUbuntu_21.10/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/home_thindil.gpg > /dev/null`

   `sudo apt update`

* For Debian 11 run the following:

Keep in mind that the owner of the key may distribute updates, packages and
repositories that your system will trust ([more information](https://wiki.debian.org/SecureApt)). In console enter:

   `echo 'deb http://download.opensuse.org/repositories/home:/thindil/Debian_11/ /' | sudo tee /etc/apt/sources.list.d/home:thindil.list`

   `curl -fsSL https://download.opensuse.org/repositories/home:thindil/Debian_11/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/home_thindil.gpg > /dev/null`

   `sudo apt update`

* For Debian Testing run the following:

Keep in mind that the owner of the key may distribute updates, packages and repositories that your system will trust ([more information](https://wiki.debian.org/SecureApt)). In console enter:

   `echo 'deb http://download.opensuse.org/repositories/home:/thindil/Debian_Testing/ /' | sudo tee /etc/apt/sources.list.d/home:thindil.list`

   `curl -fsSL https://download.opensuse.org/repositories/home:thindil/Debian_Testing/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/home_thindil.gpg > /dev/null`

   `sudo apt update`

The same detailed information about how to install each package you can find at
download page of the package. For example, for [yass](https://software.opensuse.org//download.html?project=home%3Athindil&package=yass).

##### FAQ

* How to add a new package to the repository?

  The chance that I will add a new package here is rather small. If you want
  to have a new one, you will need to create it by yourself. I can help you
  with it, use options from [contact page](contact.html) to catch me. The best
  way to have a new package is to create your own repo at [Open SUSE Build Service](https://build.opensuse.org/),
  create the package there and submit it to this repository. Of course, you
  will need then maintain that package. :) I would suggest to start with
  creating a Debian/Ubuntu package first as they probably need the most work.
  Also, Debian/Ubuntu packages require files to have proper names, when RPM or
  Arch don't. Also, your package have to be conforming with [Debian policy for Ada](https://people.debian.org/~lbrenta/debian-ada-policy.html) for `deb` packages or [Fedora Packaging Guidelines](https://docs.fedoraproject.org/en-US/packaging-guidelines/)
  for `rpm` packages.

* How to add a new architecture to existing distribution repository?

  If you want to see another CPU architecture supported by enabled
  distribution, please contact via [repository](https://build.opensuse.org/project/show/home:thindil)
  requests or if you prefer private, by options from [contact page](contatc.html).
  In that situation I will need your help in maintain the selected
  architecture, mostly with patches, and generally, using packages. :)

* How to add a new distribution to the repository?

  That's probably the hardest task. The best way is to create your own
  repository at [Open SUSE Build Service](https://build.opensuse.org/), create
  the packages which you want to add and then point me to show your work. Of
  course, the same as with new packages - you will be appointed as a new
  maintainer of that packages. :) If possible, please use for sources names
  used by Debian/Ubuntu packages system (with `.orig` before a file extension).

* I have question/idea/etc, how I can contact with you about the repository?

  Same as above, if you prefer to speak in public, use [repository](https://build.opensuse.org/project/show/home:thindil)
  requests or if you prefer private, by options from [contact page](contatc.html).

* Any other way in which I can help?

  Well, use packages, report bugs with them and report if they are outdated.
  All reports please send by [repository](https://build.opensuse.org/project/show/home:thindil)
  requests only. If you prefer other ways to support, you can look at [support us](supportui.html)
  page.
