-- layout: default
-- title: Weekly development report 2022-09-17
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

No news is good news. Thus, there are good news from the stable version of the
game. :) At least, I hope for them. Nothing to report here.

The development version of the game brings several upgrades and a few fixes to
the game's UI:

* Set the Close button as the default in the player's ship's crew member's
  inventory info.
* Added information about the current order to information about the selected
  crew member. The information contains details like, for example, what the
  selected crew member produce or train, etc.
* The change above also triggered some reorganization work in the game's code.
* Fixed position of the Close button in the show info about the selected module
  dialog.
* Fixed traversing by UI elements with Tab key when setting a skill to train
  in a training room.
* Fixed closing the skill's selection dialog after choosing the skill to train
  in a training room.
* Fixed default position of delete saved game confirmation dialog.
* Fixed setting and showing the icon for information about executing crafting
  orders.
* Work on moving the game into Nim slowly moves forward.
* The old code is still checked with AdaControl which still finds some flaws.
  Several of them fixed this week as usual. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The refactoring work is done, at least for now. It took almost the whole week,
thus the report is short again. Good news is that I finally started using the
shell. For now, only to write itself. That means I started finding bugs. :)

* Finished the second half of the work on the shell's commands' system. Now all
  the commands should be handled in the same way. Also, adding new ones will be
  easier.
* That required many changes in the unit tests either.
* Updated the code documentation, mostly related to information about imported
  modules.
* Added more information about problems when adding a new command to the shell.
* Added code to delete or replace existing shell's commands. Some build-in
  commands cannot be replaced or delete, but most of them, can.
* Fixed running the shell's aliases with arguments which contain spaces.
* Updated the backspace code, so it can delete characters also from the
  beginning and in the middle of the user input
* Added option to cancel entering a command with Ctrl-c shortcut.

### [Gameboost](https://www.laeran.pl/repositories/gameboost)

*Simple shell script to tweak FreeBSD for gaming*

And probably the last weekly change for a some time. :) I've added a setting to
set the game or application priority. This can be a bit surprising, but setting
lower, not higher priority for a game, can bring some performance boost. It
happens due the game usually wait for a system tasks when runs, like rendering
the graphic, reading from the disk, etc. Lowering the game priority gives that
tasks higher priority, thus allow them finish faster. But again, your mileage
my vary in that matter.
