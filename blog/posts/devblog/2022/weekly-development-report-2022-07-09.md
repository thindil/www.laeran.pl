-- layout: default
-- title: Weekly development report 2022-07-09
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another quiet week in the stable version of the game. Probably another missed
bugs there. :) No work in this week here.

The development version action, which could be called “beauty contest”,
continues:

* Same as in the previous week, the redesign of various dialogs goes on. In
  the week, I finished work on information's dialog about the selected item
  during trading with traders and bases. It now has buttons to start buying
  and selling the item.
* The list of items to trade also redesigned. Now it shows the selected item
  information's dialog instead of menu.
* Added a couple of new icons to the game. I'm still using icons from
  https://game-icons.net/
* Added ability to set via theming system the icons for buying and selling
  actions.
* Updated the game's modding guide with information how to change the icons.
* Fixed showing close button in showing crafting recipe and the player's
  ship's crew member dialogs.
* Fixed updating the price in buying and selling items after pressing max
  amount button.
* Changed icon for the cancel action.
* As for a long time: some code cleanup, formatting etc. work done too.

And because the last development version released almost four weeks ago, now
it is time for a new one. In around 24 hours since this post, it will be
available to download. Let's see how many unexpected features will be added
this time. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The week brings some breaking changes to the shell, but mostly work was on the
code improvement:

* Updated the project documentation with information about the shell's commands
  history and the shell's options.
* Fixed some grammar and spelling in the README.md file
* Added new types of options: text, which allow entering any text value and
  command, similar to the text type, but it checks if the entered value is a
  valid command.
* Added ability to set any program or script output as the shell's prompt. It
  should also work with multiline output. The command which will be used as
  the prompt can be set in the shell's options.
* The change above also triggered some changes to the project's unit tests.
* Fixed bug which caused that pressing Enter triggering the previously entered
  command instead of just printing a new line.
* Fixed position of the text cursor during editing a command. Sometimes it
  showed it at the wrong position.
* Again, the project documentation updated with information about how to set
  own prompt.
* Breaking change: renamed command `history show` to `history list` to match
  with other listing commands.
* Similar breaking change done to command `options show`. Now it is `options
  list`.
* The shell should now start a bit faster. Checking if proper options and
  tables in the database exists moved to the installing and upgrading part of
  the code.
