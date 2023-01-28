-- layout: default
-- title: Weekly development report 2023-01-28
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And yes, the stable version is quiet again. I could write something about
digging deeper for bugs, but I will leave it for the next week. :) Nothing to
report there.

The development version grows in its normal, slow speed:

* Fixed updating the player's ship's crew orders. Of course, the bug found one
  day after the release. As usual. :)
* I played a bit with the game's icons. Mostly with their colors, to match the
  default palette of the game. The final effects are visible on
  [the crew member inventory dialog](https://imgur.com/iwFoziZ). I think it
  looks a bit better now.
* Redesigned the dialog for giving orders to the crew members. In previous
  version, it was easy to give a wrong order to the crew member and this was
  costs some lost morale for the crew member. Now it should be more friendly
  for people who have problems with hit with the mouse, like me. :)
* As usual, the most work done with moving the game's code to Nim. Now the
  whole code related to giving or updating the crew members orders are here,
  back to moving the code related to crafting.
* And the old code got some cleanup too. As usual. :)

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

As in a new project, a lot of new things added in the passing week. The program
slowly starts to be useable. :)

* Finished work on adding support for **search** type of rules to the program's
  rules. Now both of them can be used to search for some entities in a source
  code.
* Added the last planned for now type of rules: **count**. The type of rules
  returns only amount of results for the selected rule. Additionally, it always
  returns success, no matter how many results are found. It triggered a lot of
  changes to the rule's code, but after all it made the code a bit cleaner and
  smaller. ;) Both rules should now have support for that type of rules.
* Added documentation about rules to the source code, as the modules'
  documentation.
* Fixed some problems related to the documentation about the program's rules
  and configuration. Also, updated it, so it can be used to generate the normal
  documentation.
* Added small tool to extract the documentation mentioned above from Nim code
  to the restructuredText file. The main purpose is to create normal
  documentation for the project. The work here is not finished yet, still
  generating documentation from the configuration file is to be done.
* Also, documentation on the project's page was updated with the information
  about the rules, configuration and generally the project.
