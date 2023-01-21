-- layout: default
-- title: Weekly development report 2023-01-21
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version of the game is probably stable. ;) Again, I can't find
anything bad there. Well, at least I have more time for the development
version.

Speaking of which, brings some visible changes, mostly finishing work started
some time ago:

* Fixed crash when closing the information dialog about skill or attribute.
* Added Dismiss button to the info dialog about the player's ship's crew
  members. This also required to add a new icon for the button and ability to
  set the icon in the game themes.
* Updated documentation with information about the last changes. Mostly
  interesting for people who want to modify the game.
* Fixed crash when equipping items in the selected crew member inventory.
* Removed the menu with actions for the crew members on the player's ship's
  crew list. It now just show the information about the crew member with all
  needed options. This should be less confusing than the previous version.
* Some code moved from Ada to Nim. At least I hit a milestone: now Nim is the
  second most used language in the game, according to GitHub. :) Well, still
  a long way to go here.
* As usual, some small cleanup in the old code done either.

And as every 4 weeks, it is time for a new release of the development version
of the game. In around 24 hours since this post, it will be available to
download. And looking for all new "unexpected features". :)

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

The work moves forward. This week brings a few new features to the program. I
also started using it to check the project itself, thus here are some
maintenance work done too.

* Added ability to set the program verbosity. It is based on Nim standard
  `logging` library. It allows setting the minimum level from which the program
  messages will be logged.
* As mentioned above, I started using the program to enforce some coding
  standard in the project. This triggered a lot of changes to the code. At
  least it was planned. :)
* Added option to set negation for rules. For example, it is now possible to
  find all procedures which doesn't have pragma `sideEffect`, etc.
* Added documentation about the new features to the default configuration file
  *configs/nimalyzer.cfg*.
* Updated the general information about the project on the page and in the
  README.md file.
* Redesigned how the options are sending to the rules.
* Added auto checking all the code to GitHub.
* Started work on new type of rules: **search**. They are generally similar to
  the **check** rules but at this moment the only difference is that they work
  in the opposite manner: they show results only when the pattern is found and
  return error code when nothing is found. Currently, only `hasPragma` rule has
  support for **search** type, I need to add it also to `hasEntity` rule.
