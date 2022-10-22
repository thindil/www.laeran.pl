-- layout: default
-- title: Weekly development report 2022-10-22
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The third week of preparation for the next big release after me. Again, these
weeks are too short. :) At least, the list of changes is a bit longer than the
previous one.

* Fixed showing the list of installed modules in the shipyards after installing
  a new module on the ship.
* Fixed showing information about no pilot and, or engineer for factions
  (races) which have sentient ships. This is a bigger update as it required to
  add two new icons to the game. But now it is also possible to modify them via
  the game's themes' system.
* The in-game documentation about modding updated with information about the
  new icons, too.
* Fixed bug reported by a player about crash while selling items. This one was
  interesting, as it happened only after using the sorting option on the list
  of item to trade.
* The slow work on moving code to Nim continues. At least, is seems to me that
  everything works as expected. Which means there will be hidden bugs. :P
* The old code also got some cleanup. Some things never change. Or at least,
  not too often. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

After a big week, it is time for a cleaning week. :) Generally, the past week
spent on code reorganization and testing different ways to do the same things.

* The plugins' system's code was reorganized, rewritten and refactored. :) It
  should look better now and be easier to extend with new API calls. Also, the
  shell should use a bit less memory now, especially with larger amount of
  plugins installed and enabled. The only problem is that the currently
  installed plugins may need to be reinstalled due how the data about them is
  handled in the shell's database.
* We have a first fix in this version. As usual, a few days after the release
  something bad was found. Fixed clearing the database when installation of the
  new plugin failed.
* Added a lot of code documentation, especially in plugins module.
* The tests for the shell are rewritten. Now almost each module has only one
  file with all tests related to it. This change gave really nice boost to
  running the tests. From previous 3-4 minutes to now around 1 minute. :)
  There still a few tests to merge, but that work should be done in the next
  week.
