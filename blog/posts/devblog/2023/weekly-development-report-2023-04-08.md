-- layout: default
-- title: Weekly development report 2023-04-08
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version of the game remains "stable". No new bugs reported, noticed,
etc. Something is missing there, probably my attention. :) No changes here.

The development version, as usual, proofs that weeks are too short. :) Work on
the dialog with installed modules' information continues:

* Added ability to start upgrading the engine fuel usage in the module info
  dialog. And removed the same option from the module's actions' menu.
* Added information about the state of the engine, like enabled or disabled,
  in the module info dialog.
* Added ability to enable or disable the engine in the module info dialog, and
  removed the old option from the module's actions' menu.
* Added new icon to enable or disable an engine on the player's ship.
* Added option to set the icon in the game's templates' system.
* Updated the game's modification's documentation with information about the
  last changes.
* As usual in the last months, some code moved from Ada to Nim.
* And some old code should look and work a bit better. ;)

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

The spring cleanup continues. But at least it is slowly reaching its end, thus I
hope, in the next week here will be more interesting things to report.

* Removed unneeded `validateOptions` procedures from rules. As they all use the
  version from **rules** module it is no longer needed here.
* Moved all settings of rules to one object, `RuleSettings` and removed old
  settings.
* Updated `rulesList` constant to the new version of rules' settings. Also,
  changed the constant into array instead of table.
* Renamed parameters for `ruleCheck` procedures in rules. They should be now
  more clear.
* Started work on redesign of rules code. I plan to use here metaprogramming,
  so there will not need to repeat writing of some things. At the moment, the
  work is almost done, some small changes to one template are needed. Also,
  updating the rules' code is missing. ;) This change should make changes to
  the common rules code easier.
* Fixed detecting code's documentation for templates in `hasDoc` rule.
* Fixed detecting the parameters' names in `paramsUsed` rule.
* Updated the project's documentation with information about the last changes.
* Renamed Nimble action from *tests* to *test* so it will follow the standards.
* Disabled for now usage of cache in GitHub workflow. For some reasons it
  doesn't work, workflow hangs on restoring it. I will try something in the
  next week. Maybe I will be able to fix it.
