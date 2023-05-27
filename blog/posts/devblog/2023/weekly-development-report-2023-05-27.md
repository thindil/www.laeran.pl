-- layout: default
-- title: Weekly development report 2023-05-27
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

As usual, if you dig deep enough, you will find something. ;) A bug with
training rooms in the stable version found during work on the development
version of the game. Time for the next, a bit more stable version of the game.
In around 24 hours since this post, it will be available to download.

And the development version of the game goes forward in its own speed:

* Same as in the stable version, the problem with loading saves when training
  rooms don't have set a skill to train is fixed.
* Added ability to assign the skill to train in the player's ship's training
  rooms in the module's info dialog.
* Finally finished removing the actions' menu for modules. The last action was
  setting training skill. Everything is in the same location, the module's info
  dialog. It should be easier now to reach all needed information about the
  selected module and manage it. Still no screens because the dialog needs some
  formatting. And for formatting, it requires some code redesign. Another
  invisible fun. ;) But I hope it will take less time than removing the
  actions' menu.
* Another part of code moved to Nim. Now all code related to the player's ship
  crew members are here.
* Same as almost always, the old code got some cleanup too.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

Another week spent with `fix` type of rules. Again, the code related to it
required some changes to work with the program's rules. Slowly everything is
going forward to the first version of the rules' type. There are other
changes to the program, mostly related to fixing bugs. ;)

* Added saving code updated by `fix` type of rules to files. At the moment, it
  replaces the old code with new one, thus it is a good idea to have some kind
  of backup. As the type of rules works on AST tree of code, it may produce an
  invalid code (rarely) or a reformatted code (almost always).
* Finished work on `fixRule` code for *hasPragma* rule. Now the `fix` type of
  the rule should properly add or delete the selected pragma(s) to
  declarations. Also, updated the documentation of the rule with information
  about the latest changes.
* Added `fix` type of rule to *localHides* rule. It now adds a prefix to local
  variable which hides the upper one. The documentation for the rule updated
  either with the information.
* Started work on `fix` type of rule to *varUplevel* rule. It can now replace
  *var* or *let* declaration with *let* and *const* respectively. Here is still
  some work to do.
* Updated documentation of other rules with information about `fix` type of the
  rule. It generally executes the selected command when the rule finds any
  problem.
* Fixed some typos in the project's documentation.
* Updated the project's contributing guide. There were some outdated
  information.
* Fixed detection of ability to change declaration type from *var* to *let*,
  etc. It should now better detect if declarations section contains more than
  one variable.

### [Nuklear Nim](https://www.laeran.pl/repositories/nuklearnim)

*The thin Nim binging to Nuklear GUI library*

A couple of small changes arrived:

* Added one converter and ability to get the program's window size
* Added documentation to all high level declarations not declared in Nuklear
  itself.
