-- layout: default
-- title: Weekly development report 2022-03-12
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Spending the whole time with the development version causes that the stable
version looks like it doesn't have any bugs. Let's hope it is true. :) Nothing
new here to report.

In the development version, the work with upgrading the game UI continues:

* For now, the work on the main game screen finished, except for the map, to
  which I will back later. The current version looks [that](https://imgur.com/MCeAirq).
* The start game screen also got updated images, for random names of ship, the
  player's character and for setting the character's gender.
* Work on new images for the ship info  screen started in this week.
* The modding guide updated with information how to set own images for all the
  above buttons.
* As usual, some changes under-the-hood to the game's code done. This time
  they shouldn't add any new bugs. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The work on making the shell and its code look better, slowly moving forward.

* A few more subprograms better handle exceptions. By better, I mean they don't
  propagate them, just catch and show the proper message to the user. Of
  course, the change caused some code cleanup too.
* Showing various headers for build-in shell's commands moved to its own
  procedure. This also triggered some code cleanup work.
* The form for editing the shell's environment variables now should look a bit
  better than earlier.
* Also the look of the shell's environment variables list now should be more
  clear.
* Some small changes to various messages about successful executed build-in
  shell's commands. Mostly coloring them with green color.
* Add or edit the shell's environment variable command now show message on
  success.
* Again, some tweaks to the look of the list of the last commands from the
  shell's history.
* Started work on adding types to the all variables in the shell's code. This
  should be finished soon.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This time copy and paste from the previous week. The complete week spent on fixing
the problems reported by `gnatprove`.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. Still at the graphical version of the program. :)
* Fixed showing "Clear Trash" option in the console version.
* In the console version it is possible again to restore files or directories
  from Trash.
* Fixed showing the content or information about the selected file or directory
  in the console version of the program.
* Some tweaks to the AdaControl rules setting. We will see if they will work.
