-- layout: default
-- title: Ada Linux Packages Repository
-- summary: Information about repository with Ada programming language related packages for various Linux distributions.
-- backlink: ../index.html

## General information

[Ada Linux Packages Repository](https://build.opensuse.org/project/show/home:thindil)
contains various programs and libraries related to Ada programming language
for different Linux distributions. The main goal of the project is to create a
repository of various Ada programs and libraries for different Linux
distributions and CPU architectures in one place. Also, the repository can serve
as an example for someone who wants to create own. All information related to
the repository are under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.en)
license.

Not all the packages are available for every distribution, same with various
architectures. At this moment available repositories are:

* [Ubuntu 21.10](ubuntu_21_10.html)
* [Debian 11](debian_11.html)
* [Debian Testing](debian_testing.html)
* [Raspbian 11](raspbian_11.html)

To see the full list of available packages please go to the [repository page](https://build.opensuse.org/project/show/home:thindil).

To see the lists of all available architectures and distributions, please look
to the FAQ section.

## Status

Current status of the project is **ready**.

There are several packages available, but the repository still needs some work,
mostly related to the documentation and to making packages more various
distributions standards friendly. They **should** work but they content and
names can change from time to time. Any help in that matter is more than
welcomed. :)

## FAQ

* **How to add a new package to the repository?**

  The chance that I will add a new package here is rather small. If you want
  to have a new one, you will need to create it by yourself. I can help you
  with it, use options from [contact page](../contact.html) to catch me. The best
  way to have a new package is to create your own repo at [Open SUSE Build Service](https://build.opensuse.org/),
  create the package there and submit it to this repository. Of course, you
  will need then maintain that package. :) I would suggest to start with
  creating a Debian/Ubuntu package first as they probably need the most work.
  Also, Debian/Ubuntu packages require files to have proper names, when RPM or
  Arch don't. But, before you start work on the new package, please read
  [packages requirements](packages_requirements.html) page. Another helpful
  reading is section *Tutorials* below *FAQ* section.

* **How to add a new architecture to existing distribution repository?**

  If you want to see another CPU architecture supported by enabled
  distribution, please contact via [repository](https://build.opensuse.org/project/show/home:thindil)
  requests or if you prefer private, by options from [contact page](../contact.html).
  In that situation I will need your help in maintain the selected
  architecture, mostly with patches, and generally, using packages. :)
  Available architectures depends on the selected distribution, but generally,
  are: *i586, x86_64, ppc, ppc64, s390x, armv6l, armv7l, aarch64, ppc64le,
  aarch64_ilp32, riscv64*

* **How to add a new distribution to the repository?**

  That's probably the hardest task. The best way is to create your own
  repository at [Open SUSE Build Service](https://build.opensuse.org/), create
  the packages which you want to add and then point me to show your work. Of
  course, the same as with new packages - you will be appointed as a new
  maintainer of that packages. :). Available distributions are: *Debian
  (Unstable, Testing, 11, 10, 9), xUbuntu (21.10, 21.04, 20.10, 20.04,
  18.04, 16.04, 14.04), openSUSE (Tumbleweed, 15.4, 15.3, 15.2, Factory),
  SUSE (15, 12, 11), Arch Linux, Raspbian (11, 10), Fedora (Rawhide, 35,
  34, 33, 32, 31), ScientificLinux (7, 6), RedHat (7, 6, 5), CentOS (8, 7),
  Uninvention (4.4, 4.3, 4.2, 4.1, 4.0, 3.2), Mageia (Cauldron, 8)*.
  The list can change over time as the new versions of distributions arrive
  and the old reach End-Of-Life.

* **I have question, idea, etc, how I can contact with you about the repository?**

  Same as above, if you prefer to speak in public, use [repository](https://build.opensuse.org/project/show/home:thindil)
  requests or if you prefer private, by options from [contact page](../contact.html).

* **Any other way in which I can help?**

  Well, use packages, report bugs with them and report if they are outdated.
  All reports please send by [repository](https://build.opensuse.org/project/show/home:thindil)
  requests only. If you prefer other ways to support, you can look at [support us](../supportus.html)
  page.

* **Why this repository exists, when we can create static binaries or libraries
  for Linux?**

  That's the problem, we can't create binaries or libraries which will be
  working on every Linux distribution. The main problem is incompatibility
  between various standard C libraries used by various distributions. Also, the
  GNU LibC isn't compatible with its own previous versions. And repository
  provides also way to automatically upgrade packages via distribution's update
  mechanism.

### Tutorials

All the tutorials are designed to be independent of each other. Thus, much
information, especially general, in them will be overlapping. However, it is not
required to read all of them to find desired information. But tips and tricks
tutorial requires reading the previous one.

1. [Creating simple binary package for Debian](debian_tutorial.html) describes
   how to create a simple binary package for the repository for Debian
   distribution.
2. [Creating simple library package for Debian](debian_tutorial_library.html)
   describes how to create a simple library package (exactly three packages
   from one project: library itself, development files and development
   documentation) for the repository for Debian distribution.
3. [Tips and tricks for creating Debian packages](debian_tips_and_tricks.html)
   describes tricks useful during creating a Debian package, not covered by
   the previous tutorials.
