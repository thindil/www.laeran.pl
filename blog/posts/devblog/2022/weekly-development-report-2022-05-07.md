-- layout: default
-- title: Weekly development report 2022-05-07
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version, I could say, as usual. The last few weeks were quiet
and this week suddenly a few bugs encountered. With the one on plain sigh.
At least something to report. :) Well, installing a new armor, gun or harpoon
gun on the player's ship now should work as expected. Thus, in around 24 hours
since this post, the new “stable” version of the game will be available for
download.

In the development version, the work goes in its normal pace:

 * Added limit for maximum amount of ships' modules prototypes in the game to
   1024. Currently, there are around 500 modules, so, there is some space for
   modifications. :)
 * Added limit for names of items in the game to 64 characters, the same as
   for other names.
 * Same with the names of items' types. They are also limited to 64 characters
   now.
 * All these changes again triggered a lot of changes in the game's code. Let's
   hope that not added too many bugs, either. ;)
 * As usual, updated the game modding documentation about the limits.
 * Fixed crash of the game when the player press “Move to” button.
 * Standard footer, the work on cleaning the game's code slowly moving forward.
   Really slowly, as it isn't a priority. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

A lot of new features this week added to the project. It slowly starts to be
useful shell. :)

* Finished work on editing the user's input with arrow keys. It added also
  support for insert mode to the command's edition.
* Fixed crash when only dollar sign entered as an alias argument.
* Fixed handling aliases with arguments which contain spaces.
* Generally, fixed parsing arguments of the shell's aliases. Now everything
  should work as expected.
* Added support for move in the user's input with Home and End keys.
* Again, some small changes to the project's documentation.
* Added simple Tab key completion to the user's input. At this moment it
  supports only names of files and directories, but with time I will do
  something more advanced here. :)
* As always, the simple unit test added for the new feature.
* Another new feature: now the shell colors the command entered by the user. If
  command is valid it is green, otherwise red. This code probably will need
  some optimization in the future, but for now it works.
* Started work on simple script to convert existing Zsh configuration to Nish
  configuration. Here is some work to do but should be finished in the next
  week.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Some new things arrived this week in the project. But the most time spent again
on code cleanup:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl.
* Added option to toggle visibility of hidden files and directories to the
  right click menu for the directory view in the graphical version of the
  program.
* The program documentation updated with information about the last changes.
* Started work on keyboard shortcuts in the console version of the program. For
  some reason it always runs outside my radar.
