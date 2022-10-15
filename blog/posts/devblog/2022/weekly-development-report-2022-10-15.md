-- layout: default
-- title: Weekly development report 2022-10-15
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And the second week of preparations for the next big release passed. As usual,
it passed too fast. :) This time report is even shorter than in the previous
week.

* Most of the time were spent on moving the game code to Nim. But, currently,
  the whole code related to the in-game messages system is now ported. Now I
  started moving the other parts of the code. Looks like items system will be
  moved as the next.
* The old test code related to the messages' system was removed and replaced
  with the new one. It works again. :)
* And fixed point on the agenda: some cleaning work done in the old code too.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Another big week for the small thing. A new version of the shell 0.4.0
released. Before the release arrived, a few things were added to the shell.

* Fixed compilation of the shell with orc garbage collector
* Fixed showing message about the unknown help topic
* A lot of work with code cleanup and refactoring, mostly moving various parts
  of it to new places, procedures, etc.
* The code documentation was updated.
* Also, the unit tests for various procedures updated to their new versions.
* Added command `updatehelp` to update the local help content in the user's
  database to the default shell's help content.
* As usual, added more information about the new command to the shell's help
  system.
* Added new API calls to manipulate the shell's help system, like addHelp,
  deleteHelp and updateHelp
* Fixed backspace key during editing the user's command
* Updated the shell's documentation with information about the new features and
  API calls.

After the release I started again some code cleanup and refactoring work. For
now, it is focused on how plugins are handled in the shell's code. This change
will probably trigger some breaking changes in the shell's database in the next
week.
