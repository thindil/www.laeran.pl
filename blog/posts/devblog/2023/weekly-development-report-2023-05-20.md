-- layout: default
-- title: Weekly development report 2023-05-20
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another quiet week in the stable version. I'm pretty sure soon something will
appear here. :)

In the development version, the work on the player's ship's module's info
dialog slowly going to the end. Unfortunately, still nothing to show in this
week. Also, some other changes are made:

* Fixed typos in file with list of changes.
* Added ability to assign crew members to training rooms in the module info
  dialog.
* Fixed crash during showing list of modules to install in shipyards.
* Redesigned info about the current trained skill in the module info dialog.
  It was needed for another change which will be added to the game in the next
  week.
* Again, some part of the game landed in Nim, this time the whole code related
  to saving the game. At now, it looks like it works. I will need to test it a
  bit more.
* Plus, the old code got some cleanup.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

The work on the new type of rules, continues. Looks like at the moment, most
rules will not have option to automatically fix the checked code. But work on
the rest of them required some changes to the previous code related to the new
type of rules. But here also some other changes to the project:

* Fixed negation setting for *paramsUsed* rule.
* Also fixed unit test for *paramUsed* rule with negation. It was wrong
  checking the rule.
* Updated documentation for *hasDoc* and *hasEntity* rules about the `fix` type
  of rule.
* Redesigned `fixRule` procedure. Changed its parameters and added returning
  bool value.
* As mentioned above, the work on the `fix` type of rule continues. It should
  now trigger properly for each setting of each rule.
* Added better detection if call has all its parameters named by *namedParams*
  rule.
* The above triggered a lot of changes to the code. :) But finally
  *namedParams* rule should work as expected.
* Started work on `fixRule` code for *hasPragma* rule. The work here is almost
  finished. The last thing to do is saving changes to the checked file. Plus
  do some tests. ;)

### [Nuklear Nim](https://www.laeran.pl/repositories/nuklearnim)

*The thin Nim binging to Nuklear GUI library*

That's the new thing here. I added it, because I need that thing for another,
not announced yet project(s). It is very simple and very low level binding, but
should be useable. At the moment it has support for two backends: Xlib and
SDL2. As usual, it is also mirrored on [GitHub](https://github.com/thindil/nuklearnim).
The work on the project will be very irregular, thus don't expect too much
information about the project soon. ;)
