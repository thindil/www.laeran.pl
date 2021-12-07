-- layout: default
-- title: Weekly development report 2021-05-08
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version: all the bugs which I was able to find are fixed by now.
This mean, in around 24 hours since this post a new, a bit less buggy version
of the game will be available for download. Let's see then how much other bugs
are hidden in the corners. Additionally, some unused code were removed too.

The development version: this week work was related mostly to Quality of Life
things:

* Finally, I made that the game doesn't need to install fonts on Windows.
  Also, handling fonts on Linux is now better. The side effect of this change
  is that now, the players can add own fonts to the own themes. Also, this
  change made obsolete requirement of the installer on Windows and AppImage on
  Linux. Now the game can be distributed as a simple archive. I think I will
  try this option for the next development release, we will see if it will
  work better than the old option. Unfortunately, the problem with support of
  the old versions of various Linux distribution still is here.
* Started work on adding missing ability to move in game screens with mouse
  wheel. At this moment the most of the work is done, a few screens are still
  in need to be updated.
* Some small changes to UI in various places, like added some padding to help
  text, etc.
* Same bugs which were found in the stable version, have been fixed in the
  development version too.
* And standard bottom line: under-the-hood work on better code continues as
  always. :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The whole week was spent on creating bindings for various Tk **wm** commands.
At this moment, they all should be done and work properly. Also, all unit tests
for them are on the place. The last thing to do is the code documentation for
the package `Tk.Wm`. Work on it started but still there is a lot to do.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week brings a bit more new things than the previous to the console version
of the program:

* Added option to select or deselect all files and directories in the current
  directory preview
* Added option to search by name for files and directories in the current
  directory list
* Added option to set or remove the program's bookmarks for the selected
  directory
* Fixed updating the preview of currently selected file and directory when
  going to bookmark or using path buttons
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl.

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Same as in the previous weeks: the main focus is on fixing problems reported by
AdaControl. Also, finished for now fixing various grammar problems in the user
documentation.
