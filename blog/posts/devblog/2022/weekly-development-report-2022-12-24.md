-- layout: default
-- title: Weekly development report 2022-12-17
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Foremost: happy holidays, everyone. I wish you to have a great time during
them. :)

And standard weekly report. In the stable version, a real standard. No new
bugs found this week, still [one](https://github.com/thindil/steamsky/issues/99)
which I can't reproduce awaits for help.

The development version brings even a couple of visible changes this week:

* Changed the color of the yellow progress bars to darker. The previous was a
  bit too bright compared to the background.
* Updated look of the info about the selected map cell. It now uses the same
  colors which are used by events on the map.
* The list of known events now is also more colorful. As above, it uses colors
  from the map. I think the two changes should do UI a bit less confusing. ;)
* A lot of work done with moving the game code to Nim. The code for items and
  factions are now completely moved to their new location. The only problem is
  that using the temporary code in the world generation slows it down
  noticeable. I hope to fix it before the stable release.
* And as usual, the cleanup of the old code continues. With common additions
  caused by new features. :)

And because there were four weeks since the last development release, it is
time for a new one. In around 24 hours since this post, the new development
release will be available for download. Something to check between short breaks
from eating during holidays. :P

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Cleanup week, and preparation for the next release of the shell. No new
features but removed several unplanned features, called bugs plus some code
cleanup and reorganizing.

* Added Nimble task to build the shell for Arm on Linux
* Added Nimble task to build the shell for Windows on Linux. Here I have some
  problems with GCC during linking. Not sure what causes them, maybe the
  version of GCC which I use has bugs there. While task work as expected I
  can't build the Windows version of the shell for now.
* Trying to build the shell for Windows, triggered many changes in the code,
  mostly related to the effects and exceptions handling, looks like the Windows
  version of some Nim libraries uses different effects and exceptions. Anyway,
  the work with that is done, the shell compiles for Windows... with exception
  to the problem mentioned above. ;)
* As the first release candidate for Nim 2.0 arrived I set the required version
  of Nim to 1.6.10 or below. Currently, I don't plan to update the code to work
  with Nim 2.0 yet. I will do it later.
* The most of the week spent on playing with reorganization of the project's tests.
  I plan to use command `testament all` with megatest for them, but it will
  require some work with the tests. At this moment I renamed the most of the tests,
  so they don't conflict with the project's code. There is still a work with
  adding blocks to the code.

### [Blues](https://www.laeran.pl/repositories/blues)

*The simple shell script to control Bluetooth sound devices on FreeBSD*

Again, the project revived for the week to add several changes to it:

* Added check if the user entered a proper password. I messed it a few times
  and the script behavior was a bit annoying then. :)
* Added an option to set the max amount of attempts to start the Bluetooth
  service. The previous one could create an infinite loop at some occasions.
* Moved muting the standard speakers after setting the Bluetooth service.
  Mostly to not need to manually restore them when entered a wrong password. :)
* Scanned the scrip with shellCheck. Of course, it found problems. They should
  be fixed now.
