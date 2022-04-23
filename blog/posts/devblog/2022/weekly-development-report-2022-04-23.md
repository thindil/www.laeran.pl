-- layout: default
-- title: Weekly development report 2022-04-23
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another quiet week in the stable version. Probably again I'm missing something
important. Well, for now, nothing new to report there.

In the development version of the game, the most time in the week spent again
on code cleanup:

* Added limit for maximum length of the player's ship's modules names. Same
  as other names, it is limited to 64 characters. Should be enough, if not,
  will be raised. ;)
* Added check for length to the dialog with setting various names, like ship,
  modules, crew members, so the player shouldn't enter too long name for them.
* Small redesign for dialog with information about the game crash. I planned
  to do bigger changes there, but after some tests I back to the old version
  with only few small changes. Like added button to show directory with saves
  and more detailed information about what to include in the bug report.
* Started work on some cleanups in the game's themes' system. At this moment,
  it means that some images  moved to different directories.
* As mentioned, a lot of work on code cleanup, which pretty often triggers a
  lot of changes in the game code in various places. Let's hope it doesn't add
  too many bugs. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Another week full of code cleanup, refactoring and adding unit tests to the
code. Literally, a continuation week. :)

* Code should now be properly formatted. Another small cleanup task done. :)
* Work on adding new unit tests to the code continues as in the previous week.
* Same with work on adding own types to the shell.
* Continue work on using everywhere named parameters in subprograms' calls. A
  lot of them are done, but still there a lot to do.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl.
* Changed the text on the button from *Yes to all* to more descriptive
  *Overwrite all*.
* Added missing translations strings to the program.
* Updated both, root and Polish translations.
* Of course, the program documentation updated with information about the last
  changes there.
