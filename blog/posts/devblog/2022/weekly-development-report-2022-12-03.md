-- layout: default
-- title: Weekly development report 2022-12-03
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version is under control if we speak about the work. At least for
now. :) I found two more bugs and fixed them. There is still [one issue](https://github.com/thindil/steamsky/issues/99),
but I can't reproduce it. It looks like something rare happened: or the
downloaded game has corrupted files, or maybe antivirus was checking one of
the files. Any help there would be nice. Anyway, for now, in around 24 hours
since the post, the new more stable version of the game will be available for
download.

The stable version got some small new things, mostly related to the game look:

* Factions with `fanaticism` flag now starts with maximum morale as they
  should.
* Fixed showing the amount of killed enemies in melee combat in the game's
  statistics screen.
* The in-game tables got some small updates in look, mostly related to their
  headers.
* Added a few more colors to the game's theme and started using them in the
  code instead of hard-coded ones. Now it is possible to change colors used on
  the map or for showing in-game messages. This change was also triggered some
  small changes to the game look in general. But I think I will need to work
  more on the game colors palette in the future.
* Changed icons used for buttons to cancel the player's ship destination and
  the ship's repair's priority. Now it uses the same icon as other cancellation
  buttons.
* The game documentation updated with information about the changes above.
* Journey to the Nimland in the code slowly continues.
* But it is still a bit faster than the journey to the clean old code. Which
  also takes place. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The work on Tab completion is finished for now. I started work on some updates
to the shell's look:

* As mentioned above, the Tab completion is done for now. It has now also
  support for all the shell's commands, even ones added by plugins.
* Additionally, Tab completion supports now aliases too.
* Fixed bug with aliases not returning the proper exit code of the executed
  commands.
* Redesigned a bit Tab completion for directories and files. Now it should be a
  bit faster.
* Added cleaning Tab completion after selecting one of available options.
* All tests related to the Tab completion are updated to the new version of the
  code.
* It is now possible to set the amount of Tab completion entries on the list in
  the shell's options.
* Updated the project description, as the shell slowly stops being
  "experimental" and moving towards beta stage. Which means no excuses for bugs
  or lack of documentation. :)
* As mentioned above, I started work on better look of some shell's commands'
  output. Mostly these one which presents result in a table. It added a couple
  of new external dependencies to the project, but the result slowly start be
  promising. :) Aliases, variables or history commands start looks a bit more
  modern. There still is some work to do.
