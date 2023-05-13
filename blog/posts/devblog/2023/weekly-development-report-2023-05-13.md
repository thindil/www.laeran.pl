-- layout: default
-- title: Weekly development report 2023-05-13
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version of the game seems stable. No bugs reported or found.
Suspicious as usual. ;)

The development version of the game as usual goes forward. I have probably too
much fun with breaking the game, GitHub shows that I passed the amount of 20k
commits to the code. Time flies. I'm not sure do I should celebrate it or worry
about it. ;) Anyway, in this week, only a couple of changes visible for
players:

* Added ability to cancel workshop order in the module info dialog.
* Added ability to assign crew members to medical rooms in the module info
  dialog.
* Again, some code moved to Nim. Not too much but always some progress. ;)
* And the old code got some cleanup either.

And because the last development version was released almost 4 weeks ago, time
for the new. In around 24 since this post, it will be available for download.
Many new bugs to test. ;)

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

Adding big things requires a lot of changes in the code. Just checking if you
don't sleep. :) The whole week focused on adding a new type of rules to the
program. This triggered a lot of changes to the existing code, literally a
cascade of them:

* As mentioned above, the work on `fix` type of rules slowly goes forward.
  Currently the skeleton of the code is implemented in the program, it need
  checks if the conception works.
* The work on the new type of rules triggered the redesign of `setRule`
  procedure. It was changed into template plus showing the messages about a
  rule's result now are more generic.
* And this one triggered changes in the program's rules code. :) Not only all
  of them required upgrade to the new version of `setRule` procedure. Also,
  rules messages for found and not found problems are moved to constants and
  set in rules' configuration, instead somewhere in the code.
* Another part of the cascade: all these changes caused that some parts of code
  are no longer needed, so they were removed.
* First breaking change in this version: the *hasDoc* rule stopped checking
  fields of types for documentation. I think it is not necessary, the
  documentation looks better if written outside, with documentation of the
  whole type.
* Speaking of which, the documentation of objects was updated to the new style,
  mentioned above.
* Fixed the documentation formatting for *namingConv* rule. Also updated the
  project's documentation.
