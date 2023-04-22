-- layout: default
-- title: Weekly development report 2023-04-22
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another quiet week in the stable version... probably my bug reporting system
(like mail, a couple of pages and discord) doesn't work. :) Anyway, nothing
changed here.

The development version continues its way to better UI, and breaking the code.
:)

* Fixed setting names of ships' cabins during creating ships (NPC's and
  player's).
* Added ability to set gunners for guns in the module info dialog.
* Fixed showing the list of module's owners in the module info dialog.
* Changed a bit how the information about the gun's ammunition looks in the
  module info dialog. The change was required to add a new feature, mentioned
  below.
* Added ability to set ammunition for guns in the module info dialog.
* A lot of fun with moving the old code to Nim and fixing the new bugs in it.
  Mostly related to sky bases.
* Standard footer: the remaining old code got some small cleanups too.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

And a lot of new things arrived in the project in this week. Probably, mostly,
bugs. :)

* Finished work on small tool to create the new rules for the program. It saves
  some time when creating a new rule plus reminds about changes in the
  **utils** module. ;)
* Added the new rule *varUplevel*. It can check if the declaration of a local
  variable can be changed from `let` to `const` or `var` to `let`. Most of the
  week was spent on creating the rule.
* Added unit test for the *varUplevel* rule.
* Removed completely cache from the GitHub workflow. It was causing more
  problems than helped.
* Added new parameter for `ruleCheck`: `parentNode`. It contains the pointer to
  the parent node of currently checked node. It was needed for *varUplevel*
  rule, but probably in the future, more rules will use it.
* Fixed checking if all parameters are used by *paramsUsed* rule.
* Updated configuration files for the program: added the check for the new rule
  plus updated documentation there.
* Updated documentation for a couple of rules and the project's documentation.
* Fixed checking code only when a rule is enabled.
* Removed unneeded checks from rules' code.
* Started work on the new rule *localHides*. It will check if any child
  declaration of a variable hides it with own name. At the moment, the work
  here is on a very early stage.
