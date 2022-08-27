-- layout: default
-- title: Weekly development report 2022-08-27
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The standard part about the stable version: I'm blind and nobody reported any
bug there. Thus, another quiet week there.

In the development version, the work is still mostly focused on the better
player's ship's crew members' inventory screen:

* While selecting and deselecting of items works as expected, there is still
  some work to do. I added the actions' menu to them in this week. In the next
  week I plan to add equipping and removing items, so I hope here will be
  something to show.
* Fixed some newly implemented “unexpected features” in the inventory screen.
  Like sorting items by selection status or showing information about them.
* Updated look of the dialog for moving items from the crew member's inventory
  to the ship's cargo, so it now looks like the other dialogs.
* Some work on the project documentation done too. Mostly by fixing typos or
  updating various technical information, like links to used tools, etc.
* Fixed crash during start of the game on Windows.
* As usual, a lot of work done under the hood with code cleanup and
  standardization. It seems to me that soon I will be ending the first and the
  biggest part of the work. Let's hope that other parts will take a less time.
  :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The week again bring some visible changes, mostly with finished work on the new
version of the shell's plugins system.


* Call plugins' initialization and enabling code only when they support it.
  This should made start of the shell's much faster, especially with many
  plugins enabled.
* The same done for API calls before and after execution of the user's command.
* Updated the plugins' system's documentation about the new features.
* Fixed shell's crash when the user is trying to enter a directory which isn't
  in his/her home directory tree.
* Code cleanup, all lists of the subcommands for the shell's commands now are
  handled by one procedure. This should make adding new commands simpler.
* The main work in the week is standardizing the procedures for the shell's
  commands calls. I want to do them all to return the same thing (only result
  code) and don't update the shell's history. The last will be done at the end
  of the shell's loop.
* The cleanup tasks triggered also some changes to the shell's tests.

### [Gameboost](https://www.laeran.pl/repositories/gameboost)

*Simple shell script to tweak FreeBSD for gaming*

Again, only one small change this week. I've added two more settings for Nvidia
cards, to enable or disable syncing with a monitor's vertical refresh rate and
to remove the size limit for shaders cache.
