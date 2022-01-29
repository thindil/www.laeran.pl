-- layout: default
-- title: Weekly development report 2022-01-29
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. The development toolchain is set for now. Looks like
everything almost works. :) At least no more general changes here, only some
work on the projects.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And tradition happens: one day after the new, big, stable release, a bug found.
Good thing, it is fixed. At least it isn't something critical, thus it can wait
a moment for release, so, maybe in the next week I will find something more
there.

In the development version, the work is back on the updating the look of the
game:

* The information about the selected module in bases' shipyards moved a bit
  higher, so even on small screens it should now present all information.
* Started redesigning how are various icons in the game handled. Previously,
  they were Unicode runes, what made that they were a bit hard to modify by
  someone who wanted to change the game look. I'm currently changing them to
  the vector images. Later I hope to change them on something own, but for now
  I'm using nice icons from [game-icons.net](https://game-icons.net/). I hope
  in the next week I will have something to show.
* As usual, the work on code cleanup and generally make it better done too.
  This pretty often triggers a lot of changes to the code.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This time copy and paste from the previous week. The whole week spent on fixing
the problems reported by `gnatprove`. And updating the unit tests to the new
version of the code.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Fixed crash in graphical version when trying to open the project's website
  when `xdg-open` script isn't installed.
* Added closing the *bookmarks dialog* and *create items dialogs* in console
  version with Escape key.
* Added accepting the user entry with Enter key in *bookmarks dialog* and
  *create items dialogs* in console version.
* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. Removed here the last line, so some things are
  changed. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

This one slowly is promoted to the second the most important project. :) And it
is visible, the shell is slowly getting its shape.

* Finished work on adding new aliases command. It now properly read the name of
  the new alias, by limiting it maximum length. At this moment it is set by
  constant in the code.
* Added command to edit existing the shell's aliases.
* Updated the shell's help with information about the new command.
* Updated the shell's history system. Now it stores only unique commands, but
  counts how many times each appears plus when the last time it entered. By
  default, the shell's commands' history now is ordered by the amount and last
  time used.
* Added command to show the shell's commands history information.
* Added command to clear the shell's commands history.
* Updated the shell's help with information about the new commands.
* Updated the project's documentation with information about the shell's
  aliases and the new shell's commands' history system.
* Started work on the shell's options' system. At this moment it is a new,
  empty table in database plus code to set and get the selected option. Nothing
  yet using it.
* Some code cleanup and refactoring: added default parameters to `showOutput`
  procedure and cleaned the whole code a bit.
