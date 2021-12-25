-- layout: default
-- title: Weekly development report 2021-12-25
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

First, the most important thing: happy holidays, everyone. A lot of good loot,
not only in games but also in the real world too. :) And of course, take care.
All the best for you and your relatives and friends.

Now back to the report. The stable version was quiet again. Which mean it will
be quiet by the next month either. As the development version soon will be the
next stable release, here are no more work will be done to the stable version.

And about the development version. In this week, a few new small things arrived
in the game:

* Fixed crash in boarding combat when enemy crew member has equipped shield.
  This one triggered a lot of changes in the code. Unfortunately, they cannot
  be ported to the stable version of the game. Thus, only the development
  version has fixed this problem.
* Better look of enemy ship information: now its line wrapping nicely follows
  the size of the information section.
* Added ability to resize (maximize or minimize) information sections in the
  boarding combat screen.
* Fixed crash when showing crew members' menu when there are more than one ship
  module need repair.
* Fixed showing the proper combat screen when back from the ship information
  screen to the combat.
* Fixed look of progress bars on lists when its value is zero. Mostly, it had
  an effect on showing information about destroyed ship's modules.
* Better positioning of the orders' menu. Now, it should always be positioned
  around the middle of the screen.
* Added keyboard shortcuts to resize (minimize or maximize) various information
  sections, like known bases, events, accepted missions, etc. At this moment,
  it is impossible to change the default setting yet.
* And standard, under the hood work. Code cleanup and, generally, make it a bit
  better.

Also, as mentioned above, it is a time for the next development release of the
game. In around 24 hours since the post, the new version will be available for
download. The whole work from then will be focused only on the preparation for
the release of the next stable version.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Almost copy and paste from the previous week. The whole week spent on fixing
the problems reported by gnatprove. Funny fact, adding the pre and
postconditions to various subprograms only raise for now the amount of proofs
to fix instead of reducing them. :) Anyway, the work is slowly moving forward
here.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The work here was almost identical like in the previous week:

* Finished work on adding translations to the options interface in the console
  version. At least I think I finished. :)
* Updating the program's translations.
* Made the program's menus in console version cyclic. It means that pressing
  arrows up and down buttons now switch respectively from the first to the last
  entry on the menu and vice versa.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

At this moment the shell is closer to 70s shells than a modern, but a lot of
work done in this week. It is still very short code, which still impress me. :)
And here are details:
* Added help entry for command line options.
* Better information about occurred error.
* Show tilde instead of full home directory path in the shell prompt.
* Color error messages, so they are better distinct than normal messages.
* Disabled quitting from shell with Control-C. We really don't want this,
  especially for login shells. :)
* The user's input has now maximum length of 4096 characters. Should be enough
  for everything.
* Better read the user input. Should be less error-prone.
* Added deleting the last character from input with Backspace key.
* Added very simple commands history. For now, it is only for one session,
  stored in memory.
