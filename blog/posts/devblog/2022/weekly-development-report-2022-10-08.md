-- layout: default
-- title: Weekly development report 2022-10-08
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Welcome to the first post from the "No changes on the Western Front" series.
As the preparations for the next big stable release are on the way, no new
things are coming to the game. From the other side, several bugs fixed in the
week. And these weeks are definitely too short. :)

* As usual, the worst bugs are hidden in a plain sign. The game stopped
  crashing when there is no configuration file. Which usually means, the first
  run of the game. :)
* A small update to the look of the messages' screen. It should be now wider.
* Fixed trying to open the game website link in the main menu, when there is no
  installed the proper program for it. The rare thing but happened to me (thank
  you, containers :P).
* The general information about the selected crew member of the player's ship
  should now scroll properly with the mouse wheel.
* Fixed position of the Close button in the information about the selected
  module, when there is an update on the way for that module.
* A lot of work were done under-the-hood. The game code slowly moving to Nim.
  Also, the previous code got some cleanup.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

As usual, thinking that some work is "almost done" usually means, "you are in
the middle of it". :) Another week spent on rewriting and redesigning the
shell's help system. But the rework is now finished, time for add new features
to the help. The amount of breaking changes in the code caused that the GitHub
workflow almost by the whole week was unable to compile the project. :) Below,
some details about the changes:

* All help entries are in the text file now, and they are loaded to the user's
  database when it is created. It should make editing the help easier.
* The text file with the help system content is added to the executable file as
  asset. Thus, there should be no problem with distributing the shell.
* The change above added a new dependency to the project: nimassets package.
  The project configuration and the documentation updated with information
  about the change.
* The old help system was removed. It triggered some changes to the code and to
  the unit tests of the project.
* At the end of the week I switched the Nim's garbage collector from default
  one (reference counter, which will be replaced in some time) to the one
  which someday should be the default: orc. From the one side, it raised the
  size of the executable but from the other, it also found a few problems in
  the code.
