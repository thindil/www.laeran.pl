-- layout: default
-- title: Weekly development report 2022-12-17
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Again, the quiet week in the stable version. As I'm focused on the development
version, I can't find anything suspicious here. Well, I hope that the worst
things are fixed now. :)

In the development version, there are a couple of visible changes done this
week:

* Added the help entry to the knowledge screen. As it got some improvements
  with presented information, it could be good to inform the player what all
  these colors mean. :) And now I'm also starting to think about adding that
  help to the rest of the screen. At least the ones which don't have it yet.
* Updated the game's modification's documentation with information how to
  change the newly added icons.
* Fixed some typos in the help entries.
* Added hide equip button in the player's ship's crew member's inventory if
  the item can't be equipped because it isn't a tool or a piece of equipment.
* First change to the game mechanic since a long time. ;) I noticed that
  battering rams have too strong influence on the quality of generated enemies.
  They caused to generate enemies which could be too strong, especially for
  starting players with Undead or Inquisition factions. Now, the game counts
  the installed battering ram differently, and it should generate enemies a
  bit weaker.
* I started to play a bit with some colors for the default game theme. As
  usual, it means that the most time, I'm just watching the screen instead of
  working. :)
* The work to move the code to Nim continues. A lot of code related to the
  items handling in the game is now moved. But still many things are to do.
* And the old code cleanup continues. Slowly, very slowly. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The week started with continuation of cleanup work from the previous, but ended
with adding several new small options to the shell.

* All unnecessary parentheses should now be removed from the code. It should look
  a bit better... but it is still a pretty ugly code. :)
* Added a new type of shell's options: positive. As the name suggest, it allows
  setting to that option only numerical values above zero.
* Added the shell's option `helpColumns` to set the amount of the columns when
  presenting the list of help entries to the user.
* Added the shell's option `completionColumns` to set the amount of the columns
  for Tab completion when there are more than one option is available.
* As the amount of the options slowly grows, the shell started sorting them on
  the list when presenting them to the user.
* When the user sets the shell's commands history length to zero, it now
  disables the history completely.
* Fixed deleting exceeded entries from the shell's commands' history.
* When the user set the Tab completion amount to zero, it now disables the
  completion.
* Changed the type for the shell's option `historyAmount` to positive.
* Added the shell's option `historySearchAmount` to set the amount of the
  results returned when the user is searching the shell's commands' history.
* Also, updated the shell's documentation with information about the newest
  changes.
