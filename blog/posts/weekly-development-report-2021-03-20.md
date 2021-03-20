-- layout: blog
-- title: Weekly development report 2021-03-20
-- filename: blog/posts/weekly-development-report-2021-03-20.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. Generally, the fun with static code analysis
continues in the all projects. More information are below.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

From the player point of view, the game is going currently in the worst state.
As the development cycle is close to the next major release, the current
stable version of the game is going to the attic. It means there will be no
more fixes for bugs there, all bugs will be fixed only in the development
version.

From the development version:

* Small changes to details about the selected base in knowledge screen: the
  reputation bar looks like in the stable version, show positive and negative
  values
* A bit better look for move map buttons
* Few tweaks for the available in bases missions screen and the player's ship
  info screen
* Finished for now work on [knowledge screen](https://imgur.com/dwyasbT). Now
  it presents more information about accepted missions (probably all info is
  now on the knowledge screen) and known events, especially when compared to
  the [previous version](https://imgur.com/WdS2DRg)
* As usual, a few bugs were fixed and a few new added
* The infinite task called "code cleanup and refactoring" continues under the
  hood.

The most important information: as four weeks passed since the last development
version, it is time for the next, the last before the new major 6.0 release.
Around 24 hours since this post, the new development version of the game will
be available to download. And counting to the major release will start :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Here could be copy + paste from the previous weeks. Fixing problems reported by
the AdaControl continues as ealier. `Tk.Menu` package should be finished now,
same as `Tk` itself and `Tk.Widget`, `Tk.TtkWidget`, `Tk.TtkButton` and
`Tk.TtkLabel`. Also, the unit tests were updated to the newest version of the
code. Now to do is probably the hardest part. Some AdaControl rules
produce a lot of false positive reports in the libraries (mostly with not used
subprograms), thus there will be some work now with checking all these rules
and disabling them if needed.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Another week spent almost completely on various maintenance tasks.
* Fixed crash in console version on deleting non-empty directories.
* Fixed buttons in moving items form in console version.
* Better handling special keyboard keys like arrows, Home, End, etc. Now they
  should work properly and not be triggered by normal keys (like 'd') too.
* All edit fields got option to move cursor inside them.
* A lot of work with fixing problems reported by the AdaControl.

### [Bob](https://www.laeran.pl/repositories/bob)

*Non-Intelligent console assistant (written in Ada)*

Fixing the problems reported by the AdaControl almost ended. There are still a
few things to fix, but should be done in the next week. Also, the project
documentation, especially coding standard and short information about testing
the code got update too.
