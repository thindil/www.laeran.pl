-- layout: default
-- title: Weekly development report 2022-02-12
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

This week, I fixed a bug that caused the player's ship's crew to stop cleaning
the ship if there are no sufficient tools for everyone. Thus, I think it is
time for another, a bit more stable release. In around 24 hours since this
post, a new version will be available for download.

In the development version, the work on the game UI continues:

* Still adding new icons to the game. This time not only replacing the old
  ones, but also added a few more, for better mark difference, for example
  between lack of food and low level of it.
* The game's modding guide also updated with information about the new icons.
* Speaking of modding: added maximum length for factions' indexes and names.
  Previously, they didn't have any limits. The limit is quite high, thus
  shouldn't be noticeable.
* Of course, the change above also triggered changes to the game's modding guide.
* And standard fun with the code: cleaning it plus generally making it better.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

This week brings a lot of refactorings and general code cleanup in the project.
But it also brings some new features to the shell.

* Updated `cd` command. It now also works when type only `cd`. Then it changes
  directory to the user's home directory. The code of the command moved to the
  new module. Updated information about invalid directory or lack of
  permissions to enter it.
* The whole shell's help system redesigned. The proper help entries are in the
  modules to which they belong. Also, the help system now is in its own
  module. Now, the entire code related to the help now is a little more
  clear and smaller.
* Fixed amount of last commands from history shown with `history show` command.
* Started work on environment variables system. It will be similar to the
  aliases' system, thus the work should be fast on it. At this moment the table
  for variables is added to the database and there is command to show declared
  environment variables.
* The commands `set` and `unset` for environment variables are also moved to
  the new variables' module.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This time copy and paste from the previous week. The complete week spent on fixing
the problems reported by `gnatprove`.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Added closing the *search dialog* in console version with Escape key.
* Added accepting the user search term with Enter key in *search dialog* in the
  console version.
* Removed traversing via path buttons with Tab key in the console version. It
  is start of the bigger work, which will be continued in the next week.
* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl.
