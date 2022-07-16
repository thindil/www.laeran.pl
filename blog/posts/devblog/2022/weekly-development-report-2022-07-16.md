-- layout: default
-- title: Weekly development report 2022-07-16
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Again, a quiet week in the stable version of the game. Someone has to point me
to something, what I'm missing there. :)

In the development version, the work on the next release started, after the
last week development release:

* The images for check and radio buttons changed. They should look better now,
  just I'm still not sure radio buttons. Probably in the future I will change
  them again. ;)
* Updated image for “Cancel” actions, like stop buying or selling items, etc.
* Fixed showing the Close button in the info about the known base and the
  available mission in bases.
* Fixed generating the initial equipment for recruits in bases. I have feeling
  like I'm fixing it again, or it was a different issue.
* Fixed crash when trying to buy items in bases. A new feature implemented in
  the last development version. :)
* Redesigned a bit the crafting screen. The column “Craftable” removed,
  instead added the option to show all, only craftable or non-craftable
  recipes. [Here](https://imgur.com/jVbIUAN) is a new look of the screen. It
  also demonstrates the new images for check buttons mentioned above.
* As always, some work under-the-hood with the code done too. Still “some” work
  to do.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

There were no breaking changes this week, but the work started on the new big
feature, which should bring some bugs to the shell. ;)

* Fixed crash when creating the new database for the shell.
* Moved creating the shell's variables table to the creating the whole
  database. This should make start of the shell a bit shorter as it doesn't
  check for existence of the table during it.
* Started work on the shell's plugins system. That is probably the last thing
  missed from the main goal of the shell. Also, the first version will be very
  experimental and can change a lot before 1.0 version... or even later.
  Anyway, at this moment the table in database is created and the commands to
  manipulate the shell's plugins are added. Now the work started on the
  plugins' API.
* Added a simple shell's test plugin to the tools, for checking if everything
  works correctly and as an example.
* Added the help entries for the shell's new commands.
* Fixed generating the main help screen. It was missing some help entries,
  especially from the last added things.
* Updated the project documentation with information about the last changes.
* Some small fixes for the code documentation.
* Also, a few code cleanup actions done.
