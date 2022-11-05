-- layout: default
-- title: Weekly development report 2022-11-05
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Stable version, as expected, a day or two after the release, bugs started
emerging. Fortunately for now, nothing game-blocking. Thus, I will wait one
more week before the next, more stable release of the game. Maybe I will be
able to find something more.

In the development version, the work back to updating the game's UI. And
fixing the bugs which were found in the stable version. :)

* As usual in the first week after the big release, some time spent on
  organizing the code again, like renaming some GitHub workflows, added
  information about development version, etc.
* Updated numeric fields in the game as suggested by one player. Previously
  they didn't allow being empty, always filled with minimal value. Now they
  behave more predictable, they can be empty, but then they block a proper
  button, so, the player can't send an empty form. I planned to add it to the
  big release, but I missed a few days for that.
* Fixed lack of checking of correctness of amount during setting a crafting
  recipe.
* Fixed setting maximum amount of the money to spend on training when the
  player has less money than needed for one training session.
* I hope I fixed crash when trying to move in-game dialog windows with mouse.
  I had problems with reproduce the bug by myself, so if someone is interested,
  feel free to check if the fix really works. All the three fixes are fixed in
  the stable version too.
* The work on moving the game code to Nim continues. After many changes in the
  last weeks, now it is more focused on adding code documentation and cleanup.
* The never-ending story, the old Ada code, got some cleanup and refactoring.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The most time in the week spent on adding Unicode support to the user's input
for the shell. But there also a few others, I think, small but nice additions to
the shell. :)

* Tab completion now works with commands too. Previously it worked only with
  commands' arguments.
* The code related to the syntax highlighting was moved to separated procedure.
  It triggered also adding a new unit test to the project.
* The syntax highlighting has now separated color for environment variables
  supplied to the command.
* Also, highlighting stopped marking variables as invalid commands.
* Added better detection for quoting marks in the user's input. Now the syntax
  highlighting can match the marks.
* As mentioned above, I noticed that it is 2022 (or better end of it) :) and
  added Unicode support to the user's input. Seems to me that it works, but it
  will need some tests.
* Added ability to set a terminal title when executing the user entered
  command. This ability can be enabled or disabled via shell options. By
  default, it is enabled. There is some small work to do with it. I hope I be
  able to finish it in the next week.
* Updated the project documentation with information about new things in the
  shell.
