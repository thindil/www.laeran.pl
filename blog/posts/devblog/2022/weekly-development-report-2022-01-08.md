-- layout: default
-- title: Weekly development report 2022-01-08
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. The organization work related to the change OS to
FreeBSD is now finished. There will be some changes in the future, but for now
evrything works.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The second week of preparation for the next stable release finished. Again,
not too many interesting things to show.

* The most work this week spent on code cleanup, same as in the previous week.
  And still a lot more to do. :) These changes also triggered some updates to
  the game's unit tests.
* Some updates to the ship to ship combat screen: the enemy's ship's modules
  are now “visually” destroyed after combat. The bigger change is that the
  section, which previously showed only the player's ship's damage, now shows
  all the player's ship's modules. I think it will be more consistent with the
  enemy status information.
* Breaking change for the game modding: prototypes of the mobs now can have
  only numbers as their indexes. Previously, it was possible to set also any
  string for it. It is a part of preparation of the code for formal
  verification. Soon or later, all the indexes will back again to number only
  mode.
* Technobabble: I've changed the default theorem prover for formal
  verification of the code (at this moment a very small amount) from CVC4 to
  Z3. It gives the same results, but it is around twice times faster than the
  old.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Almost copy and paste from the previous week, removed some things, so the
report is again shorter. :P The whole week spent on fixing the problems
reported by gnatprove. The work is slowly moving forward here.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous week. Thus, almost the same
report as the earlier:

* Clearing the code of the console version of the program slowly moves forward.
  The most dialogs should now have many parts of their code merged. There is
  still some work to do about this.
* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. Removed here the last line, so some things are
  changed. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The shell slowly gets its shape. But very slowly, and still is very
experimental.
* Finished for now refactoring the code and generally, trying to have it in one
  coding convention. All procedures and functions should now have proper
  pragmas included, and subprograms' calls should follow one (or two :P)
  conventions.
* Added sqlite database to the shell. For now only for setting the program's
  aliases, but later it will be storing more information related to the shell.
  Added also the option to set the path for the database from the command line.
* As mentioned above, the main focus in this week was on creating the shell's
  aliases. I want this option more advanced than it is in other shells. At this
  moment, aliases can be assigned to the selected directories and recursive
  below them, can be alias for a few commands and have support for passing
  arguments to them. There is still a lot of work to do, mostly related to the
  aliases' management commands, like listing them, adding or deleting, etc.
* Changed also how some invalid the shell's commands' results are show. Now
  they are treated as errors, not as an ordinary output.
