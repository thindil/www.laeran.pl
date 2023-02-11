-- layout: default
-- title: Weekly development report 2023-02-11
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And the stable version of the game is back to its quiet state. Which mean,
again, I should dig deeper there. At least for typos. :)

The development version brings mostly updates to the lists of in-game missions:

* As suggested by one player, added a column with information about missions'
  coordinates to the list of available missions in bases and the list of
  accepted missions.
* Added showing all available missions on the preview map when previewing the
  mission in a base.
* Added closing the list of available missions in bases when the player can't
  take any more missions, due to reaching the limit.
* Moved some code from Ada to Nim. And adding new bugs in the Nim code, as I
  don't have better things to do. ;)
* Small code cleanup in the old Ada code done too.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

As I'm slowly reaching the moment for the first release, the amount of new
features going down but the code improvements and fixes for bugs arises. :)

* Updated `namedParams` rule to show the number of the parameter instead of
  its value in the rule's messages.
* Added rule `hasDoc` to check if all public and callable entities in a module
  have written documentation.
* Added checking if all public entities in rules and the program's code have
  written documentation.
* Updated the documentation in the default configuration file.
* Updated the project's documentation with information about the new rule.
* Added missing code documentation to the project's code.
* Added `validateOptions` procedure to all rules and added checking if the
  parsed configuration file has set all rules' options properly.
* Fixed returned value for `ruleCheck` for `hasPragma` rule.
* Started adding unit tests for rules to the project.
* Enabled running unit tests in the GitHub workflow file.
