-- layout: default
-- title: Weekly development report 2022-03-26
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another week and other bugs found in the stable version. Looks like I'm back
again to weekly releases. :) As always, thank you for reporting the problems.
They should be fixed now and in around 24 hours after this post, another,
more stable version of the game should be available for download.

The development version is going forward as usual:

* The same issues which reported in the stable version fixed now in the
  development either.
* Removed Awesome Font from the game. All glyph from the font which previously
  used in the game are now images. Thus, the font is unnecessary anymore.
  Again, the game should be now a bit smaller.
* Finished work (at this moment at least) on various UI elements. The last
  thing changed are new images for check boxes and radio buttons. It should
  now be more consistent with the rest of the user interface.
* Also, the new icons for boxes and buttons should resize self when the player
  will change the size of UI font.
* Small changes to the generating missions in bases. Now, destroy type of
  missions should have much rarer enemy traders ships as target and more
  often normal enemies.
* As almost always, some work under the hood done. Mostly related to the
  code cleanup and coding style.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The work on making the shell and its code look better, going on. This week
no new features from the users' point of view.

* Another week with changes to handling exceptions in the shell. A few more
  subprograms don't propagate exception around, they all are
  nicely handled now with showing the proper error messages to the user. This
  also triggered some updates to the whole shell's code, especially for
  subprogram's pragmas.
* Finished work on adding statement `using` to the shell's code modules.
* Started work on better code documentation comments.
* Fixed information about unknown help topic. The previous was a bit enigmatic.
* Started adding unit tests for various subprograms. For now the tests are
  quite simple, just I started to learn how to use `testament` program for it.
  :)
* The project configuration updated to handle the shell's unit tests.
* The GitHub workflow also updated to execute the tests.
* Removed `debugEcho` and `echo` procedures from the code and use `writeLine`
  instead. In my opinion the both procedures should be used only in the test
  code.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This time copy and paste from the previous week. The complete week spent on fixing
the problems reported by `gnatprove`. This time also function
`Execute_Widget_Command` redesigned too. Removed the generic functions for
Float and Scalar values and replaced them with normal functions with Float and
Integer as returned values.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. Still at the graphical version of the program. :)
* Fixed showing the preview of file or directory in the Trash in the console
  version of the program.
* Removed checking for global references from AdaControl rules. It was creating
  a bit too many issues, at least with the version included in Debian
  repository.
* Added option to close Actions menu in console version with Escape key
* Fixed crash when bookmarks' directory doesn't exist.
