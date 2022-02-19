-- layout: default
-- title: Weekly development report 2022-02-19
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. Today's development log is a bit later than usual
due to some problems caused by strong wind.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Peace and quiet in the stable version of the game in this week. As usual, I
probably miss something important there. :)

The report for the development version is also a quite short this time, but the
work is going in the same pace as usual. Still mostly focused on updating the
game user interface:

* A few new icons arrived in the game. At this moment, all critical
  information should have now own icons, with difference between low level of
  resources and lack of them. Now I started work on adding separated icons for
  moving map and the player's ship. I think that some icons will be
  later replaced, at this moment I'm especially not satisfied with moving map
  buttons icons.
* Some new icons are now used also in the ship and knowledge info
  screens. But in the theme, they can be set as separated images.
* Again, the modding guide of the game updated either with information about
  setting the new icons in the game's UI themes files.
* As usual, some work under-the-hood: cleaning the game's code. This should not
  trigger any new problems.

And it is this time of the month again. :) In around 24 hours, more or less,
depends again on the strong wind around, if it broke my Internet or not, a new,
development version of the game will be available for download.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The week was opposite to the previous week with work done. This time is more
new features here that refactoring. But this code still needs a lot of work to
start looking good. Standard "newbie" code. :)

* Finished work on the environment variables system. Added all shell's commands
  related to them like adding a new environment variable, edit or delete
  an existing one.
* All the commands related to variables got also their own help entries.
* Procedure `readInput` moved to the separated module, so it can be used more
  widely.
* The main help entry is now automatically generated from the available help
  entries. I mean the section which inform about available shell's commands.
* In the project organization, I've started using Nim Action in GitHub workflow
  instead of my own docker image. It should be simpler to use. At least with
  the GitHub. :)
* The project documentation updated either with information about the
  environment variables' system.
* Redesigned the most of the subprograms to use ordinary `string` instead of
  `OptParser`. This should be a bit more effective, but we will see.
* Added support for merging commands with `&&`. At this moment, the command(s)
  after `&&` are always executed. I will soon change it to work in the same way
  as in *bash* or *zsh* shells.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This time copy and paste from the previous week. The complete week spent on fixing
the problems reported by `gnatprove`.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Finished work on new style of moving between directories in the console
  version of the program. Now it is not needed to go with Tab to the path
  buttons, it is enough to use left and right arrows to select them. Enter key
  can detect which button was pressed the last and execute proper command then:
  enter the selected via path buttons directory or activate the currently
  selected file or directory in directory view. It works in the same manner
  also during copying or moving files or directories.
* Also, the project documentation upgraded with information about the changes.
* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. At least it looks like I finally finished
  checking the graphical version of the program. Now I have to set up
  AdaControl for the console version.
