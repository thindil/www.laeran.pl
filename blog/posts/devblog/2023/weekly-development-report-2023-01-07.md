-- layout: default
-- title: Weekly development report 2023-01-07
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the first this year, the weekly development report or what was done in my
Open Source projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

A new year, new bugs found in the stable version. Several of them are caught
this week, thus in around 24 hours since this post, the new version of the
game will be available for download. And then, the cycle will start again. ;)

In the development version, again, some visible changes are made too:

* The list of orders priorities for the player's ship's crew members are moved
  to the general information about the member. One jumping window less. ;)
* Fixed crash after moving all items from the player's ship's crew member
  inventory to the ship.
* Fixed closing the player's ship's crew member inventory if it is empty,
  after moving all items to the ship's cargo.
* Fixed counting amount of work needed to upgrade the player's ship's module's
  durability.
* Again, some of the game's code are moved to Nim. It also means moving its
  unit tests to the new place.
* And not only war never changes. :) The footer is standard as usual: some
  cleanup work for the old code done either.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

A big week for the small thing. :) The new, first beta version of the shell
released. But before it happened, there were a few changes to the shell's code.
Mostly cosmetic:

* Fixed handling the user's commands' arguments. It was especially visible with
  Java-like arguments `-jar` etc. The whole code responsible for it was
  rewritten, but should work properly now.
* The most of the week spent on updating the shell's code documentation. It
  should be now cleaner better looking after generating it. Also, added
  documentation for each code's module.
* Removed some unused code. Generally, the effect is that the new version of
  the shell, with new features is a bit smaller than the previous one. ;)

And important thing: this project is coming sleep for now. I need to use the
shell for some time to see what need to be fixed, changed or added. This mean,
by some time here will be only emergency fixes, but no focus on the project.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

And the new project arrived here. At this moment everything is under
organization here, so nothing to report yet, except the project was started. ;)
As usual, it is mirrored on the [GitHub](https://github.com/thindil/nimalyzer)
too.
