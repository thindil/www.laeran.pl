-- layout: default
-- title: Weekly development report 2022-09-03
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. Today report is a bit later than usual due to some
internet shortages in my area. ;)

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another quiet week in the stable version. No problems found or reported. Looks
like I have to dig deeper. :)

The development version is going forward. This week bring many invisible
changes for players in the game code. But there is also something to show:

* Finished the first version of moving, equipping or taking off multiple items
  in the player's ship's crew members' inventory. There are still a few small
  things to add, again, I hope to do it in the next week.
* Invisible changes mentioned above, part one. The main change is that the
  first and, I think, the longest part of code cleanup and beautification is
  now complete. I've started another step in this task, but it should take a
  less time (in daily sense) than the previous one. That also triggered some
  changes in the project organization.
* Also for now almost invisible change for the players. I started some code
  refactoring work, which currently broke my testing suite (that is the only
  visible part for now). I need to look closer to this issue in the next week.
  Currently, there is no too much to say what I'm doing here. Everything is on
  very beginning part of the work. I hope to have a bit more information on
  this topic in the next week.
* Some changes to the technical documentation of the game done either. They
  are mostly related to the change mentioned above.

And because the last development release was around four weeks ago, now it is
time for another. In around 24 hours since this post, a new, shiny,
development version of the game will be available for download.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The refactoring week. That could be called this week in the project. ;) A lot
of changes are done, just they don't bring any new features to the shell, only
reworking the existing.

* The work on standardization of the procedures for the shell's commands calls
  is done. Now the most of them should take the same or similar arguments and
  return the same type of value. That task was prerequisite for the next which
  started in this week.
* Started work on the new system of handling the shell's commands. I'm trying
  to do it more flexible, so the shell's plugins will be able to add, replace or
  remove the existing commands. This will require a lot of work to make the
  whole commands' system more generalized. At this moment I'm spending
  most time in trying to find the best way to reach it. Typical fun when you
  learn a new programming language and new things. :) Anyway, that task
  triggered again many changes in the code.
* Updated unit tests for many procedures. And probably, in the next week there
  will be more changes to the tests too.
* Some code cleanup work in the shell's code and its tests.

### [Gameboost](https://www.laeran.pl/repositories/gameboost)

*Simple shell script to tweak FreeBSD for gaming*

Standard, one small change per week. :) I've added setting for Nvidia cards to
set their FXAA setting via script. Generally, it can give very small boost in
FPS in games.
