-- layout: blog
-- title: Weekly development report 2021-10-09
-- filename: blog/posts/devblog/2021/weekly-development-report-2021-10-09.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This time the list is almost standard.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

This week brings again a lot of fixes for the various bugs in the “stable”
version of the game. It should be now a bit more “stable”. :) I want to thank
all who reported any problems with the game. Now it is time to show the fixes.
In around 24 hours since this post, a new version of the game will be
available for download.

In the development version, this week report is a bit short:

* The most of the work in this week was related to fixing the same bugs which
  are found in the stable version. Plus some fixes for unique, development
  only bugs. Also,  from technical point of view, I added several unit tests,
  so there is chance that the same bugs will not happen again.
* The main game menu got “Close” entry, as suggested by one player.
* The information about the selected crew member of the player's ship's crew
  should now look [a bit better](https://imgur.com/FBi1Lzf).
* Standard footer for the last weeks (and months): a few problems reported by
  static analysis tool fixed as usual. A lot more still probably exists.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The work on *sparkification* of the bindings continues. At this moment, the
whole library is free from exceptions. This caused a lot of changes to many
bindings, but now they should be more flexible. They usually return not only
result of the Tcl command but also returned Tcl exit code and if there was
error, the information message related to the error either. Of course, it
should completely break the demo program now. :) Same as unit tests, but they
are been fixed in this week too. And at the end of the week, the library
reached **bronze** level of SPARK. Or the most of the library, `Tcl_Commands`
package due to heavy usage of pointers cannot be used in SPARK. At least not
yet. The next step will be raise SPARK mode to **prove**. This should bring a
lot of things to fix. :)

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

A lot of work was done again under-the-hood this week, but the list is a bit
longer than in the last week:

* Redesigned error message showed during creating a new file, directory or link
  in both, console and graphical versions.
* Better look for the various messages in console version.
* Fixed crash after copying or moving files or directories when the program is
  set to stay in the source directory in console version.
* Again, the main effort this week was on code cleanup, merging the graphical
  and console versions code.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Almost copy and paste from the previous weeks (this time word *Almost* was
added): fixing the problems reported by AdaControl continues. Also, the list
of rules was updated, because it was reporting problems from AWS library
either. And updated the code documentation for several things in `Server`
package.
