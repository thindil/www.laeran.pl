-- layout: default
-- title: Weekly development report 2022-03-05
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version of the game is quiet. Too quiet. Probably the worst bugs
fixed, but the small ones should be somewhere. I need to investigate it. :)

The development version going in its standard pace with updating icons for
various buttons and information:

* The buttons wait one minute and move one ship one step in path received new
  icons. There are some things to do, before all buttons related to the
  player's ship's movement will have the own icons. Thus, I think in the next
  week finally there will be something to show.
* As usual, the change above triggered updates to the game's modding guide too.
* Changed icons for buttons related to moving the game map. I didn't like too
  much the previous ones. The new should look a bit better.
* Either, the icons for buttons to expand and contract the information's
  sections changed.
* Again, some bigger changes under the hood, related to code cleanup and
  generally making it better. This time the changes even created a few new
  bugs. Fortunately, the unit tests caught them.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

After the last week the first release of the shell, the work is back to its
normal trail:

* Work on proper handling exceptions in the code continues. A few more
  subprograms are now stopped propagate any exceptions.
* The above also triggered some changes to other subprograms and mostly,
  some updates to the shell's code.
* Finished for now the work on the new version of form to add a new alias to
  the shell.
* Finished work on the new version of form to edit existing commands' aliases.
  It now has look similar to the new form for adding aliases plus also checks
  the correctness of the inserted data.
* The list of available commands' aliases has updated look too.
* Added colors to information about deleted alias.
* Shell now stops when it can't connect to the database.
* The whole shell's help system redesigned. It now should be more flexible, and
  it should be easier to add a new help entry. Also, the look of the help
  entries got some redesign.
* The list of the last commands from the shell's history also should look a
  bit better.
* The same with the list of the shell's options.
* And at the end of the week I almost finished the work on the new version of
  form to add environment variables to the shell. Again, it still needs some
  small tweaks before it will be fully finished.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This time copy and paste from the previous week. The complete week spent on fixing
the problems reported by `gnatprove`.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. Still at the graphical version of the program. :)
* Finished work on the project's configuration for checking the console version
  of the program with AdaControl. At least I hope I finished. :)
* Started work on redesign the program's menu in trash in the console version.
