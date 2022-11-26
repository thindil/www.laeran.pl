-- layout: default
-- title: Weekly development report 2022-11-26
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Busy week in the stable version. Good news: I found bugs. Bad news: they
shouldn't be there. :) Well, at least I fixed them, but as far I see there are
still a couple to fix. Let's hope that the next week will be less busy here.

In the development version, the preparation for the first release of the 8.x
series almost finished. The most time this week spent on fixing bugs and
moving the game into Nimland:

* Added separated colors, background and for fonts, in themes for tables
  headers. Also, changed the default ones to look closer to buttons as they
  now works almost the same as buttons.
* Removed ugly frames around tables, now they blend better with the rest of
  the game.
* Fixed showing the list of destroyed ships in the game's statistics screen.
* Fixed crash on finishing the boarding combat if player isn't in the boarding
  party.
* Fixed crash on entering the game's statistics screen when there is visible
  the list of killed enemies.
* Fixed starting ship for faction Inquisition and Hunter career. It should
  have a battering ram installed, not two guns.
* Fixed reading the factions' flags from data files. A new bug in the new
  code. :)
* As mentioned above, a lot of work done with moving the game to Nim. But
  still a lot more to do. :)
* Standard footer, made the old code a bit better. ;)

And as mentioned at the start, it is time for the first development release.
:) In around 24 hours since this post, it will be available to download for
all the brave who want to see the new bugs. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

New features week this time. It started with some code cleanup work but at the
end the shell got some new things. Some of them even planned. :)

* Added option to search for a command through the shell's history with
  command `history find`.
* Added help entry for the new command and updated the project's documentation
  with information about the new feature.
* Fixed getting values for short options in the user's entered commands.
* The most week spent on making better Tab completion. The whole system was
  redesigned a bit, thus should be a bit faster now. The second thing: it can
  now show a list of completions if there are more than one is available. And
  the last thing: started work on adding commands completion. Some basic system
  is done, it still requires some polishing.
* Moved code related to the setting indent of the output text of various
  shell's commands to separated procedure, so it can be easily changed. I'm
  thinking about adding an option for setting it.
