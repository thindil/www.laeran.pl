-- layout: default
-- title: Weekly development report 2023-03-11
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version of the game returned to its usual, quiet state. No errors
reported, no errors found. I think, something is there. :)

The development version of the game goes forward, as usual, in a quite slow
pace.

* Fixed refreshing the player's ship's crew members list after selecting or
  deselecting all crew members.
* Orders for all crew members, their description now change depending on if
  there is someone selected.
* Added ability to set order for the selected crew members of the player's
  ship. Currently, it uses the same orders as, giving orders to the whole
  crew. Maybe over time there will be more options available too. And for now,
  the work on the list of the player's ship's crew members is done.
* Started updating the list of the player's ship's modules, so they will look
  the same as other lists. In this week, I moved the option to rename the
  selected module to the module's info dialog.
* Added always showing the status of the selected module in the module info
  dialog. Previously, it was shown only when the module was damaged.
* Fixed crash when starting the game with debug menu.
* Fixed deleting items from a crew member's inventory when they are destroyed.
* As usual, some code moved from Ada to Nim.
* And the old Ada code also get some cleanup.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

Many changes to the code of the program, mostly related to redesign how the
program's rules work. But there is also something new to report. :)

* Updated the project's documentation, especially information about
  contributing to it. Added more details about the coding standard used by the
  project.
* A lot of changes in the program's rules code. Now, checking of the rules is
  more logical, goes from the top to the bottom of the code, not like
  previously when it was checking children of a node before the node itself.
* Added better error reporting in the program, by using the same code which now
  is used in rules' errors reporting.
* Updated GitHub workflow, so it properly uploads the program's log after
  checking the code.
* Redesigned the program's rules so they better check for their state, enabled
  or disabled with pragmas.
* Added new rule `varDeclared` to check the declarations of variables and
  constants in the code. It now can check if the declarations contains
  information about a type, a value or both.
* Updated the project's documentation with information about the new rule.
* Added checking for types and values of the variables' declaration to the
  project itself.
* Now all the program's code should have declared all or most variables
  correctly. Now I need to add that tests to the program's rules.
* Fixed crash on showing info about violated check type of test for rules.

