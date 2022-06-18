-- layout: default
-- title: Weekly development report 2022-06-18
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

While the stable version was quiet this week, there are still a few fixes for
bugs from the previous week await for release. Thus, in around 24 hours since
this post a new, more stable version of the game will be available for
download.

In the development version, the long-term work with updating the game UI
continues. This week, the most changes are in the looting empty bases screen:

* Replaced option *Take all* during looting empty bases with *Take X amount*,
  where the player can select the *X* amount to take.
* The options to take items from an empty base now appear only when the
  player has any free space in the ship's cargo.
* Added information about free the player's ship's cargo space to the looting
  empty bases screen.
* Fixed showing bonuses from skill and reputation and info about them only
  during trading.
* Changed text of action button on dialogs like buying, selling, dropping
  items from *Ok* to name of the action, like *Buy*, *Sell*, etc. This should
  be less confusing.
* Started work on some updates for items information's dialog. Now, only the
  under-the-hood work done. Nothing visible yet, thus no screenshots today. :)
* Some small updates to the game documentation, mostly fixed typos, etc.
* As usual, footer about code cleanup, etc. work added here. :P

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

This week brings some new things to the shell. But the most time spent still
on some code refactoring and cleanup.

* Finished work on adding and updating the code documentation. Now it should
  look everywhere the same. And with fewer typos. :)
* The shell's commands' history now remember also the last path in which the
  command used. When the user will query through the history or autocompleting
  the existing one, it will prefer/promoting the local commands before any
  other.
* Fixed how looks the error message when the shell can't get the command from
  its history.
* Redesigned the procedure `showError`. To show more information about the
  error if the shell built in the debug mode. Also redesigned the procedure's
  arguments.
* A lot of changes in the code to the new version of `showError` procedure. An
  interesting fact: this change reduced a bit the size of the executable.
* Some small fixes to the coding style, mostly related to not following my own
  coding style. :P
