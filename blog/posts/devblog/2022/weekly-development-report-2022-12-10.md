-- layout: default
-- title: Weekly development report 2022-12-10
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version back to its quiet state. Which probably again means that I
miss something. Well, at least I have more time to break things in the
development version. :)

Speaking of which, here the work goes as usual.

* Finished for now the work on the new version of the knowledge screen. It has
  now more colors, actions' menus for the lists entries are replaced by the
  information dialogs with buttons, so it needs less clicking to get to
  something. Here is a [screenshot](https://imgur.com/8qd9K2r) of the new
  version of the screen. This work took the most time in the week.
* The task above also required to add a new icon to the game, for setting
  various things as destination for the player's ship. The ability to set the
  icon via the game's themes is added too.
* Added using the theme colors in the list of items in the trade screen.
* The work on moving the game's code to Nim goes forward. By tiny steps.
* And cleaning of the old code is done by the way. Also, a slow way. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Generally, the updating and cleaning week. But also a few new small features
arrived in the shell.

* The work on better looking output of some shell's commands is finished. All
  headers are make now in the same way. Also, the output for Tab completion,
  when there are more than one option to choose is better formatted.
* Added new option for the shell, to set the look of the headers mentioned
  above. It is now possible to set their frames style or even completely
  disable them.
* Also added a new help entry about setting the headers.
* The project documentation updated with information about the new project's
  dependencies.
* Added prevention from crash to the shell, which mean one big "hamburger
  code". The main shell's loop is enclosed in the `try` and `except` block
  which should prevent the most problems.
* And started another cleanup work. I decided to remove unnecessary
  parenthesis from some functions calls, for example `string.len` instead of
  `string.len()`. The code is almost cleared now I have to finish it and clear
  the tests too.

### [Blues](https://www.laeran.pl/repositories/blues)

*The simple shell script to control Bluetooth sound devices on FreeBSD*

Revived the project again for a couple (literally) small changes:

* Added better check for starting Bluetooth FreeBSD services. My new headphones
  need more tries to get connected. ;)
* Added check if the user entered the password. If not, simpy stop the script.
