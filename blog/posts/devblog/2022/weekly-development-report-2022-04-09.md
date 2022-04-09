-- layout: default
-- title: Weekly development report 2022-04-09
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another week, another bug reported by the player in the “stable” version.
This one could be even funny if it is not crashing the game: the in-game
clock can go further in hours than the planned. I was able to end with 29
hour in a day. :) Anyway, it is fixed now so, in around 24 hours since this
post there will be a spam in a couple of places about availability of the
new version of the game.

In the development version, the whole week spent on various cleaning tasks:

* Added maximum length for ships' names. Now it is set the same as other
  names (NPC's, bases) to 64 characters. Should be enough for now, if not,
  it will be raised.
* Added information in the game's modding documentation about maximum length
  of the description and name for the ships and their prototypes.
* Added maximum length for ship's prototypes' indexes.
* All these changes triggered a lot of other changes in the code and in the
  unit tests.
* As usual, the work on code cleanup slowly moves forward.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The cleanup and refactoring tasks took the whole week. At least some of them
are finished or finishing now. Plus the code slowly starts looking good. :)

* Finished work on better handling exceptions in the shell's code. Now all
  subprograms should not propagate any exception but show nice information on
  what happened. As usual, it also triggered some changes in the entire
  shell's code.
* Continue work on better code documentation comments. That work is almost
  finished, unless I again miss something in the code. ;)
* Continue work on adding unit tests to the project. Most of them are still
  very basic tests, but they slowly start working.
* Started work on using own types of variables instead of generic ones. It
  should not only make code more readable but also in the future more safe. At
  the moment when I will start using `distinct` types.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. This time something big changed: the graphical
  version is done, now the work started on the console.
* Fixed moving between windows in the console version of the program when the
  last keys used were left and right arrows.
* Added option to close About menu in console version with Escape key.
* Changed text on the *No for all* buttons in the console and graphical
  versions of the program to *Cancel*. In my opinion it is more understandable.
* Fixed AdaControl GitHub workflow to not check for AdaCurses package. This took a
  few tries, but now it works correctly.
