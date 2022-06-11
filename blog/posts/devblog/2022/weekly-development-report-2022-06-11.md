-- layout: default
-- title: Weekly development report 2022-06-11
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version: The best time for finding bugs is a day or two **after**
a release. This rule worked this time. I fixed them, but they have to wait for
release because there is scheduled a new development version soon. There is a
small change too, now the game doesn't show empty inventories of crew members,
just info that the inventory is empty.

Speaking of which, here work going as usual:

* Finished work on coloring the in-game help. Now it can be almost
  [a rainbow](https://imgur.com/XC3M2LC).
* Added ability to change the help's colors via themes system. It should be
  helpful for colorblind people or just people with better taste. :)
* The documentation about modifying the game updated, too.
* Same issues as in the stable version, fixed in the development either.
* Same as in the stable version, now the game shows only info about empty
  crew member inventory, not the inventory itself.
* Redesigned the dialog for giving items from the ship's cargo to the crew
  members. It looks a bit different. The main change is that it can count the
  maximum amount of items to give, based on the selected crew member's
  inventory's free space.
* As always, a lot of code cleanups and bringing some consistency to it. At
  least it is now around 75% done.

And as mentioned above, in around 24 hours since the post, everyone will have
opportunity to tests all the changes. A new, development version of the game
will be available for download.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Still no new features this time. The whole week spent on playing with the
code cleanup and refactoring.

* Finished work on using `.type` notation in the code. There is still the old
  style in the unit tests, but for now they will stay there.
* Added lock level information to some procedures and functions.
* The work on making a couple of types **distinct** is finished for now too.
* Most of the new types are moved to separated modules. It should make the code
  a bit more readable and predictable.
* Same as in the previous week, the changes above triggered a lot of changes to
  the code. But it should be upgraded now too. At least it compiles. :P
* The unit tests are updated either with the new types and their locations.
* Added tests for the all new modules. Same as with the previous tests, they
  are basic tests and need some love in the future.
* Started work on adding and updating the documentation for the new types.
