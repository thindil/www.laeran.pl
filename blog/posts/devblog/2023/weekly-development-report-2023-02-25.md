-- layout: default
-- title: Weekly development report 2023-02-25
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

While nothing new detected in the stable version of the game this week, the
fixes from the previous week are ready to deploy. Thus, in around 24 hours
since this post, a new "stable" version of the game will be available for
download.

In the development version, there is even something to show. :) But most work
again are invisible for the players:

* Fixed showing the last empty column in some tables, mostly in buying recipes
  in bases.
* Added columns with coordinates to the lists of known bases and events. Now
  the knowledge screen looks [that](https://imgur.com/GpncUni).
* Fixed color for distance column in the list of known events.
* Moving the game code to Nim goes forward, now all things related to crafting
  are in the new place and I started breaking the code related to prototypes
  of mobs.
* Old code got some cleanup too. Small amount as usual. :)

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

Fixing found bugs are finished so it is time to start implementing new...
features of course. :) Also, some refactoring work done this week:

* Fixed the returned result for negation for `namedParams` and `paramsUsed`
  rules.
* Fixed internal returned results for violation rules `namedParams` and
  `paramsUsed`.
* Added a lot of new tests for rules `namedParams` and `paramsUsed`.
* Reorganized the project's tests. As the test for each rule looks almost the
  same, only data is different, I moved common code to the separated template
  and in the tests set only the data for testing. Now the tests are a bit
  cleaner plus adding new rules should be easier.
* Updated the project's documentation with information about configuration
  file.
* Added ability to set as an optional parameter a parent entity to `hasEntity`
  rule. If it is set, the rule will check only childs of the entity with the
  selected type.
* Started work on adding ability to set as an optional parameter an index of
  child to check to `hasEntity` rule. If it is set, and the parent entity is
  set, the rule will check only the selected child for the selected parent.
  The work is almost finished, there are some small fixes to do yet.
* Updated the project's documentation with information about the latest
  changes and fixes.
