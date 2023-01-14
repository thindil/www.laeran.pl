-- layout: default
-- title: Weekly development report 2023-01-14
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the first this year, the weekly development report or what was done in my
Open Source projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version returned to the most common stage: all bugs are hidden,
nothing emerged this week. As usual, I probably have to dig deeper. ;)

In the development version, some small visible changes are done:

* The work to redesign the UI related to managing the player's ship's crew
  members continues, with the speed of a small iceberg. :P I've added a button
  to show the crew member's inventory to the general info about the crew
  member.
* Added option to set the icon for the new button via the game's theming
  system.
* Finished updating the game tests. I merged them all into one mega-test.
  Effect: previously it took around 10 or 15 minutes to check them all. Now
   it takes around 3 minutes. :)
* A lot of work done with moving the game from Ada to Nim. For now, it looks
  like everything works as expected, or better, the old bugs are ported too.
  :P
* Some standard code cleanup for the old code done either.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

The project slowly takes it shape. To be honest I'm a bit surprised how fast
everything is going here. Many configuration options are on the place, there
are two rules to check are added.

* The program now has a couple of options, how to set the list of files to
  check: from listing every file to recursive go through the selected
  directory.
* As mentioned above, the program offers two rules to check at this moment:
  `havePragma` to check if callable routines (procedures, functions, etc) have
  proper pragmas and `haveEntity` to check if the selected entity like
  procedure, variable with the selected name exists in the module.
* Also the whole parsing code was redesigned and rewritten. Now it should work
  better.
* Added a lot of documentation about the program settings into the
  *configs/nimalyzer.cfg* file. Later I will add a real documentation, but for
  now, as the whole API is liquid, these things change quite often.
* Fixed the program compilation in GitHub workflow. For some reasons, nimble
  there can't find compiler source code, thus it needs to be downloaded
  separately.
