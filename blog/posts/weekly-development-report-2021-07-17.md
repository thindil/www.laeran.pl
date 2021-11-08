-- layout: blog
-- title: Weekly development report 2021-07-17
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version, a couple (literally) bugs were found this week. Also,
the in-game help was updated, and it is now a bit more grammar friendly. This
mean I'm ready to release another almost stable release of the game. :) As
usual, in around 24 hours since this post, the new version will be available
to download.

In the development version, work continues as usual:

* Finished, for now, the work on the list of available missions in bases. Added
  last things like pagination and some small fixes.
* The same problems which were discovered in the stable version of the game are
  fixed in the development version too.
* The most visible change in this week: added possibility to move various
  dialogs around with the mouse. From one side is nothing big, but I like the
  final result. :) I was trying to record it, but unfortunately, my screen
  recorder refused to work. Looks like I need a new screen recorder.
* The technical documentation of the project was updated either. Mostly, I
  added info about coding standard used by the project and testing process,
  things interesting probably only for programmers. ;)
* As always, in the last months, some work under the hood in code polishing:
  clearing it and some refactoring.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The work on `Tk.Winfo` package as bindings for various Tk **winfo** commands
continues. As usual it triggers some changes to the other packages either. For
example, type `Window_Geometry` was moved to package `Tk.Widgets` so it can be
used by `Tk.Winfo` package either. Also, the unit tests for the new subprograms
were added. Still a lot of work to do there thus, probably in the next week the
report will be very similar to this. :)

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week brings a few new things to the console version of the program.

* Work on executing the user defined commands in the console version is
  finished. Now it also showing the commands output in the same way like in the
  graphical version of the program.
* Added option to clear the system Trash in the console version.
* Starded work on showing the content of the system Trash in the console
  version. At this moment it is early work in progress. But I hope it can be
  finished in the next week.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

As usual, quite short report here: fixing the problems reported by AdaControl
static analyzer continues. And probably will take some more time. At least now
I'm at `Messages` package. Also, I started adding more unit tests to the
program. At this moment only packages `Layout` and `Config` got them, but
the other packages are waiting in the line for them too.
