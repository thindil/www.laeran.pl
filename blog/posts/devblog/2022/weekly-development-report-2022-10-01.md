-- layout: default
-- title: Weekly development report 2022-10-01
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Again, nothing to report in the stable version. Which means, from now, the
stable version is going to sleep for the next four weeks as the whole focus
will be on preparing the next big stable release of the game.

In the development version of the game, there were several changes to the game:

* Fixed showing the title of the player's ship crew member's information dialog
  when it contains a scrollbar.
* Fixed position of the Close button in the player's ship selected module
  information dialog.
* Fixed look of information about level of tiredness and health of the crew
  members in their information dialog.
* Made progress bars related to the information about the player's ship crew
  members statistics, skills and experience wider.
* Changed the title of the player's ship crew member information dialog.
* Added option to rename the selected crew member in his/her information
  dialog.
* Removed the option to rename the selected crew member from his/her actions'
  menu.
* Added better Tab traversal to the information dialog of the player's ship
  crew members.
* Added closing the crew member's information dialog with Escape key.
  [Here is the screenshot](https://imgur.com/ALVrHFH), how the new version of
  the dialog looks.
* As usual, some work with the code cleanup done too. Some things probably
  never change. :)

And because the last development release was four weeks ago, it is time for
the next. :) In around 24 hours since this post, the last development version
(before the big one stable) of the game will be available for download. And
then, the next four weekly reports will be monotonous due to focus on fixing
bugs and not adding any new things to the game.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The next shell's system which currently is rewritten or updated is the help
system. The idea is to move all the help content to the text file and load it
from there to the shell's database during creating the shell's configuration.
The whole week spent on implementing it, but the work is almost finished.

* Created the text file which contains the content of the shell's help system
  and slowly fill it. Most modules have moved help there, still some work
  left to do.
* Updated the shell's code to the new help system as the work goes forward.
  Also, some code were removed as unneeded, code documentation updated and a
  few other small organization tasks done to the code.
* Updated unit tests to the new version of the help system. Same as with the
  code, some tests were removed as unnecessary.
* Updated the command to run tests in the GitHub workflow. It was using the old
  one and reporting that everything is ok. :)
* Updated the project documentation, like link to the Contracts package, fixed
  some typos, etc.
