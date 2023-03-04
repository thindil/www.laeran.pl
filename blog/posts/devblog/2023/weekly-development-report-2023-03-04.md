-- layout: default
-- title: Weekly development report 2023-03-04
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Again, in the stable version of the game, peace and quiet by the whole week
after the newest release. Perhaps, people prepare a long list of problems. :)

The development version has some visible changes, but they are a part of a
bigger, not finished yet work, thus, text only report this week:

* Fixed possible crash when saving the game to the file.
* Started work on ability to give orders only to the selected player's ship's
  crew members. Currently, only the list of crew members is updated with
  ability to select the crew members for orders. Also added ability to select
  or unselect all crew members. It can be useful in a situation when the player
  wants to give an order to all but one crew members.
* Moving the code from Ada to Nim continues. As usual, it starts in the one
  place and I have to go deeper in the code to move other things too. This
  sometimes looks like [yak shaving](https://en.wiktionary.org/wiki/yak_shaving). :)
* And of course the constant update to the old code continues. At least it is
  around the half of the last stage. ;)

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

The week started with adding new features to the program and ended with
documenting them:

* Finished work on adding ability to set as an optional parameter an index of
  child to check to `hasEntity` rule. Also added support for negative index of
  the child. In that situation the index is counted from the end of the list of
  children of the node.
* Some code cleanup, now all rules use the same code to show information about
  issues during work. The information also contains full stack trace, if the
  program was compiled in the debug mode.
* Added a new feature: ability to disable rules in the checked code with
  pragmas. It allows disabling a selected pragma for a part of the code and
  re-enable it later. All rules should now support the pragmas. Where exactly
  the pragmas should be places, it depends on a rule. Some rules are able to
  find the pragmas in any place, others only in the specific locations. It may
  be unified over time, but we will see. ;)
* Updated the project's documentation with information about the program's
  pragmas and how to use them in the code. Also, each rule got information how
  to use pragmas with them.
