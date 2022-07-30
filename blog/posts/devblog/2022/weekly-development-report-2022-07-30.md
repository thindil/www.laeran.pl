-- layout: default
-- title: Weekly development report 2022-07-30
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Looks like this month will pass without any new stable releases. No changes in
the stable version of the game in this week.

In the development version, the fun with updating the game UI slowly moving
forward:

* More dialogs' buttons now showing icon and text at the same time.
* Updated crafting interface. Same as in trading, pressing the mouse button on
  the list now showing the information about the selected crafting recipe
  instead of the actions' menu. The actions themselves moved to the dialog with
  information about the crafting recipe.
* Added information where the selected recruit has equipped its items on its
  inventory list.
* Similar to the crafting interface, the recruit interface updated. Now, when
  clicking on the recruits' list, it shows the information about the recruit.
  Additionally, added a new icon for hiring/negotiating action button.
* As usual, the new icon can be set via the game's themes system. The
  documentation about the game's modification updated with information how to
  do it.
* All buttons in the recruit interfaces in bases now show icons and text on
  itself.
* As usual, a lot of work with code cleanup and generally made it more
  readable. Still some work to do.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The big week for the small thing. Another alpha release 0.3.0 arrived this
time. After a short celebration (the whole 5 minutes :P) I back to work, the
list below contains mostly changes which appeared in the release:

* Added API to get response from a plugin. Currently, it is used only when
  taking more information about the plugin, when showing details about it.
* Added API to trigger enabled plugins before and after the user entered
  command.
* Finished work on the first version of the plugins' system of the shell. At
  this moment it is very basic and unoptimized system, but I hope over time I
  will do something more useful there.
* Added unit tests for various subprograms related to the plugins' system. At
  this moment it looks like everything works as expected.
* Added documentation about the plugins' system, in the README.md file and on
  the project's webpage.
* As mentioned above, after some tests and final updates to the project's
  documentation the new version of the shell arrived.
* And the work on the next version of the shell started as usual with some
  improvements to the code. This time I started adding contract based
  programming to the shell. At this moment it is in very early stage of
  setting. Looks like I will have to do some more changes to the project's
  configuration to have everything to work as expected.
