-- layout: default
-- title: Weekly development report 2022-09-10
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. Today report is a bit later than usual due to some
internet shortages in my area. ;)

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The state of the stable version is as usual: no bugs found or reported, thus
no changes here. Well, at least I have more time to spend with the development
version. :)

Speaking of which, the work progressing here in the standard speed:

* Many changes in the project organization this week. Looks like my experiment
  from the previous week works. Some time ago, I've decided to try to rewrite
  the game in the different programming language. This time I selected an even
  less popular language: [Nim](https://nim-lang.org/). The main issue is that
  I didn't want to completely drop the old code and start the work from
  scratch. Another problem to solve was to not stop developing the new things
  in the game. I think I solved both concerns. I replaced some old Ada code
  with the Nim version, plus added some new things to the game. It will take
  some time to rewrite the game completely, and it still will be in the
  playable state. The only victim of the change are the old unit tests. They
  will be replaced with the Nim ones, but I was forced to disable the old one
  for now.
* Finished for now work on the player's ship's crew member's inventory. It now
  allows selecting, unselecting all items and equip, take off or move to the
  ship's cargo the selected items. A new look is [here](https://imgur.com/q9SH5zm).
  I'm still not sure about the icon for unselecting. Maybe I will change it
  some day.
* Standard footer from the previous weeks: fixed a couple of issues reported
  by AdaControl in the old Ada code.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The refactoring work continues. Again, many changes in code but all of them
still invisible for the users. At least, as long there is no new bugs. :)

* The work on the new commands' system for the shell continues. I think I'm
  currently in around 50% of the things to do here, thus I hope to finish it in
  next or two weeks. Same as before, this task requires many changes in the
  code, but at the end, it should be a bit better organized and prepared for
  adding new commands. Same as in the previous week, most time is spent on
  finding a good way to solve issues than on solving them. :)
* A lot of changes in the unit tests related to the shell's commands code
  triggered by the task mentioned above.
* Fixed and updated the code documentation for some procedures.

### [Gameboost](https://www.laeran.pl/repositories/gameboost)

*Simple shell script to tweak FreeBSD for gaming*

Another weekly change. :) I've added settings for Windows games when running
them by Wine. These settings should give nice boost to FPS and fix a few issues
with that kind of games.
