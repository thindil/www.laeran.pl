-- layout: default
-- title: Weekly development report 2022-10-29
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Time for the last boring update before the big release. And then, probably as
usual, will be time for weekly more stable releases. :D The work on the next
stable version is done. As usual, I didn't have time to add everything what I
wanted. Well, at least I will have something to do with in the future. The
list of changes for the past week is a bit short:

* Fixed bug with information about tools needed to train Metalsmith skill.
* Fixed the information about starting bases in the new game screen. This one
  is the best example, that I'm blind: I was looking on it by a few years and
  didn't see it. :) Better late than never.
* Fixed the game hangs on the start a new game when the player selected a base
  type which is unavailable for the selected faction.
* Some work with moving code to Nim. A part of reading the game data from
  files is moved. Still more work to do.
* And the old code got some cleanup as usual.

As mentioned above, in around 24 hours since this post, the new release of the
game will be available for download. I will then post a short roadmap in the
announcement, as always, for the work towards the next version of the game.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Another cleaning and maintenance week. Most of the changes focused on code
cleanup, reorganization or fixing bugs. Suddenly there a lot of them emerged.
Probably because I started using the shell more often. :)

* Updated the code documentation and added new ones for many procedures. Mostly
  related to the new version of the shell's plugin system.
* Fixed ability to set the shell's `promptCommand` option by the user. For some
  reasons it was set as a read-only option.
* Added pragmas for new code in the shell's plugins system. It allowed to find
  a few more issues in the code which should be now fixed.
* Fixed coloring environment variables in commands as invalid.
* The shell's test plugin got some updates for better handling arguments sent
  to it.
* Fixed not working special keys in some terminal emulators.
* Updated the project's documentation with information about how to set or
  reset `promptCommand` plus some style fixes for the documentation. And with
  information about the last changes to the shell.
