-- layout: default
-- title: Weekly development report 2023-04-01
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Very busy week:

* Implemented full real time combat
* Finished the last 3D assets for ships
* Added some new music to the game (now it is 100 mins in total)
* Rewritten the game in [Whitespace](https://en.wikipedia.org/wiki/Whitespace_%28programming_language%29)
  programming language.

Of course, happy the Dad's Jokes' Day, everyone. :) Back to the normal report:

Well, week after the new, more stable release and nothing new to report in the
stable version of the game. Again, people probably too busy with creating the
full list of problems, and I'm blind because I don't see them. ;)

In the development version, the visible work is still around the dialog with
information about the player's ship's modules. But also other work done:

* Added ability to start upgrading the cabin's quality in the module info
  dialog. And removed the same option from the module's actions' menu.
* Added ability to stop the module's upgrade in the module info dialog.
* Added ability to start upgrading the engine's power in the module info
  dialog. As above, the corespondent option from the module's actions' menu
  was removed.
* Fixed showing information about the current upgrade in the module's info
  dialog.
* Some part of the code moved to Nim. Another milestone reached: now more than
  10% of the game's code is ported. Now, all the code related to the ships'
  prototypes are in Nim.
* The old code also got some cleanup and updates.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

Definitely spring cleanup week. Many changes to the code related to its
organization. It is mostly preparation for adding new features and rules, but
it ends also in a lot of code cleanup and reduction.

* Now all the program's rules use the same code for setting the result of the
  check. This mean that all common code for rules should be in the same place.
* Fixed detecting the documentation comments of modules by `hadDoc` rule.
* Updated compilation flags for Nim 1.6.12 - **loggging** module uses generic
  *Exception* exceptions and generate a lot of warnings in the code.
* Added `validateOptions` procedure do the rules module to use it instead of
  the same name procedure in the program's rules. The rules themselves now will
  set only several settings instead of creating the whole procedure. Now only
  removing the old code from the rules is to be done.
* Updated GitHub workflow, so it will be using the newest version of Nimble for
  managing dependencies.
* Updated unit tests for rules. They now check the whole own output, thus they
  should now catch more problems. ;) Also, almost all tests are updated for the
  new `validateOptions` procedure.
