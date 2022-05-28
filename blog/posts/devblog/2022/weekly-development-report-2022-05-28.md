-- layout: default
-- title: Weekly development report 2022-05-28
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Looks like finally I start finding the problems. ;) During  the work at the
development version of the game, I also found a few small, not crashing issues
with shipyards in bases in the stable version. All fixed, but I will wait one
more week, maybe I will find something more there.

Speaking of the development version, this week there is even something to show.
:)

* The same issues which found in the stable version, fixed now in the
  development either.
* Finished work, for now, related to the redesign of how information about the
  ship's modules look during installation. I added automatic comparison between
  installed and to install modules. If there are more installed modules, the
  player can select which he/she wants to compare. For example, comparison of
  guns looks [that](https://imgur.com/AAN658x).
* Also, when showing information about the gun to install, the game now shows
  only general information about the ammunition needed, instead of listing
  every possible ammunition. This should make the look more clear.
* Some typos fixed in the documentation related to the project.
* The standard work on code cleanup and beautification continues as almost
  always.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Almost copy + paste from the previous week. The whole week spent on playing
with the code of the shell.

* Finished work on updating the unit tests to use `LimitedString` too. Now, the
  unit tests should work as expected.
* Finished updating `LimitedString` related functions with pragmas.
* Started work on adding unit tests for `LimitedString` type. This is just a
  beginning of the work, thus probably it will take a lot of time in the next
  week.
* Added constant `EmptyString` to `LimitedString` but it will be probably
  replaced in the next week. I need to check a few possibilities for that.
* I raised the minimum needed version for Nim to 1.6.6. It should work with
  previous 1.6.x versions but the most time I'm testing it with the newest
  stable, thus only this version is 100% guaranteed for now that everything
  works as expected.
* Also, fixed some bugs caused by changing using standard `string` type to
  `LimitedString`. Now everything should work as expected.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week is continuation of the work from the previous one:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl.
* The program documentation updated again with the information about the last
  changes visible to the users.
* Added showing the about menu with the keyboard shortcut in the console
  version of the program.
* Added selecting or deselecting all files and directories in the current
  directory with the keyboard shortcut in the console version.
* Added showing rename files and directories form with the keyboard shortcut in
  the console version.
* Added entering and leaving copy files and directories mode with the keyboard
  shortcut in the console version.
* Added entering and leaving move files and directories mode with the keyboard
  shortcut in the console version.
