-- layout: default
-- title: Weekly development report 2023-02-04
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

If you are looking deep enough... then someone will finally point you to the
problem. :) One player found some problems with the Independent faction in the
stable version and reported them. They are now fixed, so in around 24 hours
since this post the more stable version of the game will be available for
download.

In the development version, all things as usual, going slowly forward:

* The problems with the Independent faction are fixed here too.
* Added option to give "Go rest" order to the whole player's ship's crew.
  The main usage of it will be probably resetting the crew members to their
  default orders or positions on the ship.
* Added an icon for the new crew order.
* Added option to set the icon for "Go rest" order in the game's themes.
* As usual, updated the game's modding documentation with information how to
  set the new icon in a custom theme.
* Nim slowly eats Ada, as in the last few weeks. :)
* Also, the old code should be a bit better now, after cleaning it a little.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

Again, a few new things arrived this week in the project. Also, a couple of
bugs found and perhaps fixed. ;)

* Finished work on *gendoc* tool to generate the project's documentation from
  its code and configuration. It should now also follow the coding standard of
  the project.
* Added Nimble task to build HTML version of the project's documentation.
* Updated the documentation of the project with information about the last
  changes to it.
* Added the new rule: `paramsUsed`. It is looking in the code if all callable
  declarations, like procedures, functions, etc. use all their parameters.
* Added the new rule: `namedParams`. It is looking in the code if all calls
  have declared their parameters as named.
* The project's documentation was updated with information about the new rules.
* The project's code was checked and fixed with the new rules. ;) This took the
  second part of the week.
