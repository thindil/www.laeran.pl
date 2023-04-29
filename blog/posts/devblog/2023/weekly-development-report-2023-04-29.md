-- layout: default
-- title: Weekly development report 2023-04-29
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version still in sleeping more. A month without bug reports.
Suspicious as usual. ;)

Work on the development version is going with its normal speed:

* Added the new icon for setting ammunition for the player's ship's guns
  button.
* Also added ability to set it in the game's themes.
* The game's documentation about modifications updated with information about
  the new icon.
* Added ability to start upgrading battering rams damage in the module info
  dialog.
* Some code moved to Nim. More code related to the sky bases are now in Nim.
* And, as usual, some small cleanup of the old code done either. ;)

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

And another big week for the project. The new alpha version, 0.3 released. But
before it happened a couple of things landed in the program:

* Finished work on the new rule *localHides*. It can now find all local
  variables with the same names as previously declared ones.
* Added unit test for the rule *localHides*.
* Added ability to disable test for search for invalid code. It is done mostly
  due to *localHides* rule.
* Added a new rule *namingConv*. As its name suggest, it checks if various
  declarations in a code follow the selected naming convention. It can check
  variables, procedures and enumeration fields. The naming convention is
  regular expression.
* Added unit test for the rule *namingConv*.
* As mentioned above, the new release 0.3 arrived. :) All changes below this
  line are in the repository version of the program.
* Fixed typo in changelog
* Better check for naming parameters in *namedParams* rule. Now it checks also
  dot calls, like `myString.split(';')` and can check nested calls inside
  calls.
* Updated the project's documentation with information about the latest
  changes.
* Started rewritting some templates z **rules** module into macros. The main
  reason is to remove ugly things like `{.inject.}` pragmas and unnecessary
  `{.ruleOff.}` pragmas.
