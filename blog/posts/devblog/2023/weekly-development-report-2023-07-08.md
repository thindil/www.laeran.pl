-- layout: default
-- title: Weekly development report 2023-07-08
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Welcome to the last development report for the stable 8.0 series of the game.
As by most time, no changes in the code here. I have a feeling that the next
big version will have a lot more bug fixing releases available. ;) As the
last development version will arrive soon, the next four weeks again will be
focused only on the preparation for the new major release.

And the development version itself. Some visible changes are again arrived
here, but I started to test the game for bugs. Of course, they are here. ;)
Some of them are squashed, but I think there are still a lot more to find:

* As one of the players suggested, added the ability to remember the messages'
  window's size on the map. Now, when switching the game's view and returning
  to the map, the game should remember the size.
* Redesigned the dialog for setting boarding and defending parties in the
  combat. Same as with setting crew members' orders in the ship's info screen,
  it now has the confirmation button before the order is changed. This was done
  mostly for consistency of interface, but should also prevent a large morale
  loss when the player can't decide about who should be assigned to the party.
* Fixed saving the information about what type of upgrade is make for the
  selected module in the player's ship.
* Fixed crashing the game during undocking from bases.
* Again, a lot of code moved to Nim. Now all the game's data related code, like
  reading them from files, is in the new place.
* And the old code got some cleanups. The standard footer. :)

As mentioned above, it is again the time for next, the last development release
of the 9.0 series of the game. In around 24 hours since this post, it will be
available to download. And then the "boring reading" month will start. No new
features will be added, only bug fixes (probably a lot) and code cleanups.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

The work steadily goes toward a new, still pre-alpha release. The work on the
rule `ifStatements` is finished for now and another rule arrived in the
program. Plus the new rules are applied to the project itself, which caused a
lot of style fixes in the week. ;)

* As mentioned above, the work on the rule `ifStatement` is done for now. The
  test for the rule added, its documentation is mostly finished. Some small
  changes to the documentation probably will be made in the next week.
* The project's documentation now have the section about the structure of the
  program's rules' code. It is mostly useful for people, who wants to add new
  rules to the program or edit existing ones. In the section there are
  information about variables, procedures, macros and templates used in
  creating the rules.
* Updated the code to work with Nim 1.6.14. It means mostly changes to the
  GitHub workflow file.
* Fixed some typos and grammar issues in the project's documentation.
* And the program's new rule arrived: `forStatements`. As the name suggest, it
  checks the `for` statements in the code. At the moment only if the statements
  have or don't have direct call to `pairs` or `items` iterators. It can also
  add or remove these calls from the checked code. Most of the work is done here
  (again), but there is still something to do, like documentation and unit test
  for the rule. Almost déjà vu. :)
* The program's code updated to the new rules. Many `for` loops are changed to
  have consistency in the coding style.

### [Wine cellar](https://www.laeran.pl/repositories/winecellar)

*A graphical user interface for managing Windows programs on FreeBSD*

The work on installing a new Windows application resumed. Now the code related
to install a Wine version from [Wine-Freesbie](https://github.com/thindil/wine-freesbie)
project is almost finished. The "only" this to do is to test it. ;) It should
be done in the next week.

