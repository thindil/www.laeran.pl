-- layout: default
-- title: Weekly development report 2022-08-13
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Yet another bug found in the stable version, for some reason the game doesn't
show information about change of items to break. It should be fixed now. Again,
in around 24 hours after this post, a new, let's hope, more stable than usual
version of the game will be available for download.

The development version is going forward. But my to-do list is still long. :)

* The game should present correctly the chance of items to break. Same as in
  the stable version.
* Fixed showing information about the items in the player's ship's crew
  members' inventories.
* Added new images to the game, for moving items from the crew members'
  inventory to the player's ship's cargo and to wear or take off the items.
* Added ability to set the new images via the game's themes system.
* As usual, updated the modding documentation with information how to set the
  new images.
* Added button to move items from the crew member's inventory to the player's
  ship's cargo and to equip or remove the item.
* Changed behavior of the crew members' inventory list. Now it shows the item
  info dialog instead of an actions menu as earlier.
* The standard footer: the work on code cleanup and beautification going
  forward.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The whole week spent on adding contracts to the various procedures. And tasks
related to them.

* As mentioned above, the most of code should now have added contracts, but
  there is still some work to do. I think I will end this task in the next
  week.
* It triggered some changes to unit tests too. Now all the tests should work
  properly again.
* Made procedure `showError` discardable so it doesn't require `discard` word
  any more, as it used a pretty often in the code.
* The whole shell's code updated to the new version of `showError` procedure.
* Added or updated some code documentation.

### [Blues](https://www.laeran.pl/repositories/blues)

*The simple shell script to control Bluetooth sound devices on FreeBSD*

Only one small change this week. Fixed restoring the sound settings after stop
a Bluetooth device. For some reasons, FreeBSD reset the kernel setting
`hw.snd.basename_clone` to zero after stopping Bluetooth services, which
prevented for example, sndio from works. Now it should work properly.

### [Gameboost](https://www.laeran.pl/repositories/gameboost)

*Yet another simple shell script to tweak FreeBSD for gaming*

Another new thing here. As the description says, it is a very simple shell
script to tune the FreeBSD settings for gaming. Same as with Blues, I've done
it mostly as my backup for now. At this moment, it is available here and on
[GitHub](https://github.com/thindil/gameboost).

