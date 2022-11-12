-- layout: default
-- title: Weekly development report 2022-11-12
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The plan was to release a new, more stable version on this Sunday, but today I
found a few bugs related to filtering the items' lists. The game doesn't show
all items' types available, for example in the trade screen. So, the release
is postponed now to the next week until I will fix all of them. And probably
find something more right before release. :)

In the development version, the main focus was again on the game's UI:

* Another player's suggestion added: numerical fields to sliders. There are no
  too many of them, but it took some time to implement all of them.
* Added prevention of moving in-game dialogs outside the game window. No more
  hiding them somewhere, now they always stay visible. ;)
* Added some colors to the lists of known bases and events. In bases, the
  visited ones have green color. In events, the colors are the same as on the
  map: dangerous events are red, positive one are green. I'm still thinking
  about some more upgrades related to the lists. Maybe add a separated color
  for base, event or mission which is currently set as target for the ship?
* Fixed position inside some numeric fields after editing them. It now should
  be correctly at the end of the entered number.
* Fixed loading the weapons prototype items from files. It seems that it wasn't
  loading all available weapons.
* Slowly, but moving the game's code to Nim is going forward. This time, some
  part of code related to items are moved there.
* Standard footer: the old code got some cleanup too.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Very similar week to the previous. It seems that my Unicode support wasn't
perfect (read: was full of bugs :P) so I spent more time with it. But again,
also some small new things arrived in the shell.

* Added setting the terminal's title at the start of the shell. This should
  finish the work on the feature for now. Unless someone will bring some
  interesting ideas to it. ;)
* Fixed a few typos in the project's documentation.
* Added option to enable or disable the syntax highlighting in the user's
  input.
* Added error messages in a few places with information when something related
  to the user's input go wrong.
* Fixed Unicode support for various the shell's forms, like setting aliases,
  variables, etc.
* Better editing of the user's input in various forms. Now it is works very
  similar to the normal input, with exception to no history, syntax highlighting
  or insert mode.
* Updated the project's documentation with information about the new features
  and changes.
* Again, a lot of work related to code cleanup or refactoring. At this moment
  the main focus with that is to merge the code related to the user's input.
  That causes to appear also more code documentation and unit tests. ;)
