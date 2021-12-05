-- layout: default
-- title: Weekly development report 2021-10-30
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Again, after the release, the stable version is suspiciously quiet. Sure,
here are a few problems to fix, but all of them require a lot of changes in
the code. Thus, they are a work in progress in the development version.

Speaking of which, in the development, the work in this week focused mostly on
the new versions of various in-game menus. Generally, their look and feel is
almost the same as it was in the old stable version. I completely forgot that
the current look should be only temporary. At least, I will make all in-game
menus to look similar to each other. :) Some details about the work:

* Work on the orders' menu finished for now. The new is
  [a bit less ugly than the old one](https://imgur.com/QZYd3DF).
* Work on the [new version of the main game menu almost finished](https://imgur.com/CfoJ6NU).
  There are still some small quirks to fix, but that should be done in the
  next week. At least keyboard shortcuts should work now in the menu too (that
  is one of the bugs mentioned in the stable version).
* Small work on the project organization, and more specifically, renamed some
  steps in one of GitHub workflows.
* As usual, “a few” changes to code which are not brought anything new (I hope
  bugs either) to the game but should do the game code a bit cleaner.

And because the last development version released almost 4 weeks ago, it is
time for another. In around 24 hours since this post (hello beloved by
everyone time change) the new version will be available to download.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The work on code *sparkification* and fixing bugs continues. Again, nothing new
added to the library, but a few more Gnatprove checks are passed. Just with
this speed it will take a few months. :) Anyway, some creating widgets
subprograms are verified. This required to move `Options_To_String` functions
to the packages specifications (for use them in contracts) or to move the code
related to conversion to the new functions (and then, made it visible for
contracts). Also, a few problems reported by AdaControl fixed too.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The effect of finished the work on clearing the project's code is finally
visible. This week brings a few more things to the program, mostly fixing
various problems in the console version:

* During copying or moving files and directories, using bookmarks change the
  destination directory, not the source. This change is in graphical and
  console version of the program.
* Added bookmarks' menu when copying or moving files and directories in the
  console version.
* Fixed crash in console version during moving or copying files and directories
  when the user activates any file.
* The messages' window should now look better in the console version. Its size
  is now dynamically counted.
* Some small code cleanups done too.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes.

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

And finally, the work here is finished for now. :) The code should look a bit
better. Some problems reported by AdaControl tool should be fixed too. The
separated GitHub workflow for the AdaControl moved to the main workflow, after
the unit tests. Also, the project's and the code documentation was updated
either. And yesterday, the great day for the small thing arrived: a new version
3.0 is available for [download](https://www.laeran.pl/repositories/yass/wiki?name=Download):
it is the first version which officially works on Windows too. At this moment,
the project is going to sleep mode, to give me some time on a few bit more
secretive projects. :) All of them are related to Ada programming language.
