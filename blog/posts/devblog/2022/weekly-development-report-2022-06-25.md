-- layout: default
-- title: Weekly development report 2022-06-25
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

After the release, the stable version of the game is quiet again. Which
probably means I'm missing something again. :) Nothing changed here in the
past week.

In the development version, the whole week spent on updating the look of
dialog with information about an item in the player's ship's cargo.

* Changed the look of buttons in the dialog. They now show icons instead of
  text. Of course, new images for the buttons added too. ;) The biggest
  problem here was not breaking other dialogs, they still can have a text
  instead of icons. It looks like everything works properly, but it needs
  some more testing. When the buttons have set image instead of a text, they
  also have tooltips, which should help a bit. There is still some work to do,
  mostly related to the general look of the buttons, that's the reason today
  no available screenshot.
* Added possibility to set the button's icons in the game themes.
* The change above also triggered changes to the modding the game
  documentation.
* Changed how item management in the player's ship's cargo works. Previously,
  clicking on the item was bringing the menu. Now it shows the dialog with the
  item's info and actions buttons. I think it should be a little better option
  that the previous one.
* As always, fun with code formatting, updating, refactoring, etc. continues.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Another week with some new things in the shell. This time even more new things
than under-the-hood code cleanup and refactoring. ;)

* Better handling the updates of the shell's database. Now the database has its
  own version for the schema and generally, the updating code should work even
  with a few versions below the current.
* Added read-only settings to the shell. That kind of settings is used mostly
  internally by the shell, user can only view it but not change it. At this
  moment only the shell's database version is set as a read-only option.
* Added the shell's options to set by what to sort the `history show` command
  output. It is now possible to sort it by amount, name and last used. Also, it
  is possible to set order of the sort. This change required to add a new type
  of setting value.
* Fixed look of `options show` command output. Mainly related to aligning the
  table columns, as they were a bit desynchronized after the last changes. :)
* Updated the shell's help's entry about `history show` command. It now informs
  not only about the amount of commands to show but also how they are sorted
  and the sort order.
* Updated the shell's documentation with information about the new features and
  changes.
* Plus, as usual, some code cleanup, formatting and generally trying to make it
  better. In typical for someone new to a programming language style. :)
