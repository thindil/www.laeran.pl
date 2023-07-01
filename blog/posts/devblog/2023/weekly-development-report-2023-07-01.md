-- layout: default
-- title: Weekly development report 2023-07-01
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

A new month and again nothing to report in the stable version. It means that
probably the current stable version will remain in that state. There is just
one more week before release of the last development version for 9.0 version
of the game, thus no too much time to find any bugs. ;)

In the development version, a couple (literally) of changes which are visible
and useful for the players arrived:

* Added information about types of bases to the game's help. Same as for
  factions or careers, it shows the same information which is available on the
  new game screen.
* Added ability to select or unselect all crew members for boarding an enemy
  ship or defending the player's ship in combat.
* The most time this week spent on moving an old code to Nim. Now, all the code
  related to the game's missions are in their new home. A lot of code related
  to the game's help were moved, either.
* And the old code got some standard almost infinite cleanup. ;)

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

Week like a roller-coaster ride. ;) Started with stopping work on external rules
feature and ended by almost finished adding a new rule.
Again, some new features arrived this week. This time it also brings some
breaking changes. After all the project is still in pre-alpha stage. Mostly due
to lack of features and tests. ;)

* GitHub workflow file updated with build the release version of the program
  for Windows and FreeBSD. Also added build the release version for Linux.
* As mentioned above the work on external program's rules continued by some
  time. Unfortunately, the option with support them as dynamic loaded
  libraries also didn't work. Looks like in Nim 1.6.12 there are some
  problems with `llStreams` and using them from C. Also, creating the program's
  feature require a lot of changes into the code. I'm not sure if it is even
  needed. Adding a new rule to the program and recompiling it, is currently
  quite simple. So, the work on the feature stopped, and all previous changes
  related to it are removed from the code.
* Added the new program's rule: `ifStatements`. As its name suggests, the rule
  runs various checks against `if` statements in the checked code. Currently, it
  can detect:

   1. Empty statements (only with `discard` statement).
   2. `Else` branches which are after "final" statements like `return`, `break`,
      `raise` or `continue`.
   3. Negative conditions in statements which have `else` branch.

  The rule can also fix the code by removing, replacing or moving the code. The
  work here is almost done, there are still a couple of issues to fix and create
  any documentation for the rule. But generally it works, the program uses it
  now too. :)

### [Wine cellar](https://www.laeran.pl/repositories/winecellar)

*A graphical user interface for managing Windows programs on FreeBSD*

Only changes related to the Nim binding for Nuklear library arrived this week.
Added `using` statement plus ability to set the amount of items on the list to
show in a combo widget.

### [Nuklear Nim](https://www.laeran.pl/repositories/nuklearnim)

*The thin Nim binging to Nuklear GUI library*

Time for the monthly update. ;) The changes from Wine Cellar project arrived
here. Plus small updates to the project's documentation.
