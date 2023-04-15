-- layout: default
-- title: Weekly development report 2023-04-15
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Still no reports about bugs in the stable version. And I probably don't see
something obvious. Nothing to report here.

The development version visible changes are related mostly to the dialog with
information about the player's ship's module:

* Fixed crash when encounter an enemy ship after loading the game.
* Fixed size of module's info dialog. Now, it should not hide the Close button.
* Added ability to set owner for a cabin in the module info dialog.
* Added ability to set the icon for assign crew button in themes.
* The documentation about the game's modification updated with the information
  how to set the new icon.
* Added ability to start upgrading guns damage in the module info dialog.
* Some old code was rewritten in Nim. That should bring some new bugs. ;)
* And the old code got some updates too.

Because the last development release was almost four weeks ago, it is time for
the new. In around 24 hours after the post, the new development version of the
game will be available for download.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

The code cleanup, refactoring etc. tasks are finished for now. It is time to
start adding new features. I planned to add one thing but due to some
problems with the compiler I postponed it for later. So, probably this release
will bring mostly new rules plus a lot of changes to the program's code.

* The whole week spent on fun with GitHub workflow various fixes and changes.
  Mostly related to handling the project's dependencies and the GitHub cache.
  There are still some things to test, but I hope to end this task in the next
  week.
* Moved all common rules' code to templates in **rules** module.
* Rewritten all rules to use templates. It removed a lot of code from the
  project. :)
* The task above brought one more feature: now the pragmas to enable or disable
  rules in the code can be used in any place of the checked code for all rules.
  Earlier some rules required to place them in specific locations.
* Updated documentation of rules, so all of them should now present the same
  level of information.
* Started work on small tool to create the program's new rules. At this moment
  it is very basic tool but should create at least very basic skeleton of a
  rule.
* Also, I have tried some other approach to handle the project's dependencies,
  especially the compiler's source code. It still needs some work.
