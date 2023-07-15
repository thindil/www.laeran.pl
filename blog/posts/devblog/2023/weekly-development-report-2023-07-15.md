-- layout: default
-- title: Weekly development report 2023-07-15
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And welcome to the first weekly development report from "boring and short"
series, before a next major release of the game. I started testing the game and
as expected, the bugs arrived. :) The whole week spent on bugs fixing and
updates to the game's code:

* Fixed bug with generated NPC's ships starting with docked speed, so the
  player can always escape them.
* Fixed crash when the game deletes an expired event.
* Fixed showing Ask For Events button even right after asking for them.
* And fixed that crew members don't need to rest or consume anything (my
  favorite). :)
* As usual, some code moved to a new home, the work now is on moving creating
  a new game there.
* The never-ending story with updating the old code continues slowly forward.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

Another big week for the small thing. :) A new alpha version, 0.5 released. But
before it happened, there were some work done. Plus, after short, 1 minute
celebration, the work on the project resumed. And the new code brings some
breaking changes to the program's configuration.

* The for on the rule `forStatements` finished. Added all tests for it, even
  all passed after fixed some problems. :)
* Updated the project's documentation with information about the new rule.
* Here was the new alpha release. :)
* Made the program's configuration's file's syntax case-insensitive. Now
  settings like `source`, `Source` and `sOuRcE` all are valid. But please don't
  use the last one. :)
* Added code for `fix` type of `paramsUsed` rule. Now the rule can remove
  unused parameters from the subprograms' declarations. Can be breaking change
  if someone earlier used it just to execute `fixCommand` setting.
* Added check for empty `for` statement to `forStatements` rule. It works on
  the same way as in the `ifStatements` rule, removes `for` loops which
  contains only `discard` statement.
* Definitely breaking change: added option to set which checks perform for
  `forStatements` rule. Now all or just one of them can be selected. The option
  is now required, thus it breaks compatibility with the previous version of
  the program's configuration.
* And a lot of updates to the project's and the changed rules' documentation.

### [Wine cellar](https://www.laeran.pl/repositories/winecellar)

*A graphical user interface for managing Windows programs on FreeBSD*

Same as in the previous week, the work on installing a new Windows application
continues. Installing a Wine version from [Wine-Freesbie](https://github.com/thindil/wine-freesbie)
project is finished and working properly, after fixing a couple of issues. ;)
And now work will start on installing the application itself.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

And the almost annual update to the website done. No, the ugly, standard look
will stay. :P The contact page got some updates with information about me and
new ways to contact with myself, plus the website footer was changed to give
link to the contact page instead of Matrix.
