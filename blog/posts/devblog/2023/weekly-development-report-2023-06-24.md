-- layout: default
-- title: Weekly development report 2023-06-24
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another week without changes to the stable version. Well, I have a feeling that
the next major stable release will have a lot more to report in the matter of
bugs. :)

The work in the development version comes in it normal pace. This week brings
changes visible and even useful for players. ;)

* Fixed look of the base's info dialog when the player's reputation in it is
  unknown.
* Added information about available in-game factions (races) to the in-game
  help. It now shows the description of factions and relations with other
  factions, like enemy or friends.
* Fixed updating the map after the movement of the player's ship.
* Added information about available the player's careers (professions) to the
  game. Similar to the factions' info, it shows the description of careers and
  list of skills which have bonuses to experience from that career.
* Some old code replaced with the new written in Nim. Mostly related to the
  missions' system.
* And remaining old code got small updates too.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

Again, some new features arrived this week. This time it also brings some
breaking changes. After all the project is still in pre-alpha stage. Mostly due
to lack of features and tests. ;)

* **BREAKING**: Made check for correctness of custom options' values
  case-insensitive. Now `typeFields` and `typefields` are equal. This is
  breaking change at the moment only for *hasDoc* rule, which had option with
  upper and lower case letters.
* Changed name of `typeFields` to `typefields` of the configuration option for
  *hasDoc* rule. This is breaking change only for development build, not
  releases.
* Rule *hasDoc* now can insert the selected template of documentation into
  various elements of checked code. The template has to be a text file in
  reStructuredText syntax, used by Nim documentation. The example of that
  template can be found in the rule's unit tests directory.
* Speaking of which, tests for *hasDoc* rule was updated for checking `fix`
  type of the rule.
* And the project documentation was updated with information about the `fix`
  type of *hasDoc* rule.
* `genrule` tool got some updates in preparation for add a new big feature of
  the program.
* Added testing do the project builds on Windows and FreeBSD in the GitHub
  workflow. After a couple of bugs, looks like everything works. :)
* And the work started on the mentioned big feature: external rules for the
  program. Currently, I'm looking for the working way to add the thing. :) The
  first try was using Nim scripts as the external rules. Unfortunately, a lot
  of `compiler` package code works only in compilation mode. Now I'm testing
  the second option: external rules as dynamic libraries. At the first glance,
  it looks good, but I need more time for implement it and test. This work
  should take some time, so the next week report will be probably a lot shorter
  than this. ;)

### [Wine cellar](https://www.laeran.pl/repositories/winecellar)

*A graphical user interface for managing Windows programs on FreeBSD*

The work continues in slow pace. Now the program has a simple *About the
program's* dialog and started work on the user interface for adding a new
Window's application. This mean that the program now also downloading
information about available [wine-freesbie](https://github.com/thindil/wine-freesbie)
versions from the GitHub and detect installed Wine versions. Not too much but
still something to show. ;)
