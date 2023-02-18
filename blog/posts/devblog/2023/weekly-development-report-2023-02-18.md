-- layout: default
-- title: Weekly development report 2023-02-18
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

When looking deep enough, it is possible to find something to fix. For
example, something visible, like the lack of pagination buttons for the list
of known bases. ;) It is fixed now, plus added the check to be sure that the
game always gives correct amount of game's points after finishing a goal. I
will look by one more week to check if I can find something more. Because I'm
sure there is something. :)

In the development version, most changes are not visible to players:

* Optimized a bit the code for drawing the map. Generally, it shouldn't be
  noticeable, but it was breaking the new missions' preview. So, two targets
  with one shoot. :)
* Fixed resetting the map's preview after ending it.
* Same as in the stable version, fixed showing the pagination buttons for the
  list of known bases.
* Also added here the check to be sure that the game always gives correct
  amount of game's points after finishing a goal.
* Moved almost all code related to the crafting system into Nim. Still a lot
  of work in this task. ;)
* And the old code got some small cleanups.

As usual, because the last development version of the game was released almost
four weeks ago, it is time for the new one. In around 24 hours since the post,
it will be available for download.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

And the first alpha release of the program, 0.1.0 arrived. As expected, the
best moment to find the bugs in the project is a few days after a release. :)
Generally the whole week spent on hunting for bugs and fixing them:

* Added better handling dependencies in the Nimble configuration file.
* Started work on better tests for the project. This mean not only more tests
  but also some code refactoring. As slowly some pattern in the tests appears,
  I will probably spend here some more time to rewrite them completely, so it
  will be easier to add new one. But for now, adding new tests shows that the
  program has a quite large amounts of bugs, especially related to the negation
  for rules. ;)
* Fixed the returned result for negation for `hasDoc` and `hasEntity` rules.
* Added a lot of new tests for rules `hadDoc`, `hasEntity`, `hasPragmas`.
* Fixed internal returned results for negation for `hasDoc` and `hasPragma`
  rules.
* Updated the project documentation with information about the latest changes
  (or better, fixes).
