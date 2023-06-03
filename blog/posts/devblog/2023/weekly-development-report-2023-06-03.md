-- layout: default
-- title: Weekly development report 2023-06-03
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And the stable version back to its quiet state. At least, I hope it means fewer
bugs. ;) Nothing to report here this week.

The development version still no things to show, or better, there are some
things broken due to work on them, so it is better not show anything. :)

* Fixed crash when showing info about the player's ship's gun with assigned
  ammunition.
* Continue work on the look of the player's ship's modules' info dialog. In
  this week, I finished reorganizing information there by moving them up or
  down on the list. In the next week I will need to shift the work's priorities
  as the bigger change in look comes there.
* Again, some part of the code moved from Ada to Nim. This time it is
  generating events code. It also generated "several" bugs, which I'm still
  hunting.
* The old code got some cleanup as usual. No new bugs reported here. ;)

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

And the work on the `fix` type of rules is finished for now. At the moment,
most rules just execute a command set by the user when they meet any
problem. But some of the rules are capable to auto fix issues. Also, the unit
tests of the program got some updates.

* Finished work in `fix` type of rule for *varUplevel* rule. The last added
  thing was disabling the type for negation of the rule.
* Added more information about `fix` type of rules to the project's
  documentation.
* Fixed some typos in the documentation of *varUplevel* rule.
* Added ability to disable all or just negative tests for `fix` type of the
  program's rules. Also, disabled the tests for most of the rules. *localHides*
  and *varUplevel* rules have disabled only negative tests for `fix` type.
* Added tests for the `fix` type of rules.
* The previous change as usual, revealed some issues with the implementation of
  `fix` type of rules. Now, the code should be fixed and works as expected. By
  the test of course. ;)
* Added more information to the tests output about what test is checked in the
  present moment. It triggered a lot of changes to the program's rules tests.

### [Wine freesbie](https://github.com/thindil/wine-freesbie)

*Various versions of Wine for FreeBSD*

One big update under the hood. I changed GitHub action used to build Wine
versions. It allowed to add support for FreeBSD 13.2. Now I'm slowly build all
available Wine versions. As usual, it will take some time in the next week too.
