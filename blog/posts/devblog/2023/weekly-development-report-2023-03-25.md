-- layout: default
-- title: Weekly development report 2023-03-25
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version, I found several more issues to fix. Only one more is to
do, thus tomorrow a new a bit better looking and a little more stable version
of the game will be available for download. It starts looking like a new
tradition, one release per month. :)

In the development version, the main visible work is still focused on the
player's ship's modules' info dialog:

* Updated look of module's info dialog for cabins. Their cleanliness and
  quality information is shown in the same way as their durability info.
* Added ability to start the upgrade of the player's ship's module's durability
  in the module info dialog. The same action removed from the module's
  actions' menu.
* Fixed crash on looting empty bases screen, when the player's ship's cargo is
  bigger than the length of the items list to loot.
* Fixed crash during cleaning the ship in an open space.
* Updated documentation about modifying the game, with information about
  setting the icon for starting upgrades buttons.
* Slowly moving the code to Nim.
* Even slower, cleaned a bit the old code. :)

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

The week started with big thing: a new version of the tool released. After
around 5 minutes of celebration the work back on the trail. This week mostly
code reorganization tasks, preparation for start working on the big thing for
the next update. But this will require a lot of changes to the program's rules
code.

* Fixed documentation for configuration files syntax. Its name was conflicting
  with the name of **config** module. Now the project's documentation should
  render itself properly again.
* Fixed `hasPragma` rule return value when a declaration doesn't have any
  pragmas.
* Reported the program to the [nimble packages' database](https://nimble.directory).
  Now it should be easier to install it for someone.
* Started work on refactoring the program's rules' code. At this moment all
  common imports of modules are moved to the **rules** module, so their don't
  need to be written in the rules code. The second thing, almost done is to
  move summary information of the rules to one procedure in **rules** module. The
  more advanced refactoring just started, so its results will be visible in the
  next week.
* Tests for the new procedures are added either.
* Fixed regression: `hasEntity` rule again detect properly the selected
  entities.
* Updated the program's documentation with information about installation. But
  also about the last fixes. ;)
