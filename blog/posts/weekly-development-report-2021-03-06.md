-- layout: blog
-- title: Weekly development report 2021-03-06
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. Generally speaking, the most of the week (in some
projects even all) was spent on fun related to the static code analysis and
fixing problems reported by it. Now a bit more details.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another week which passed too fast :) Work on polishing the game UI continues.
At least, this time here will be something to show.

* Finished work on various question's dialogs. Now they should look on every
  supported operating system that same.
* Fixed look of the game statistics after ending it (on the player death).
* Probably finished work on [ship information screen](https://imgur.com/Mb2pX3Q).
  I think it looks a bit better than [a few months ago](https://imgur.com/9dh1dEe).
  Also, should be more user-friendly.
* As usual, a lot of work were done under the hood. Mostly code cleanup plus
  fixing problems reported by the static analysis tool.
* Added some more tooltips to the various UI elements. Especially in the combat
  screen.
* One of the players found a way to use the nightly builds of the game, and now
  he started reporting bugs :) Thus, in this week a few more bugs than usual
  were fixed.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Fixing problems reported by AdaControl continues. `Tk` package should be good
for now, same as `Tk.Grid` and `Tk.TtkButton`. The work now started on fixing
package `Tk.TtkLabel`. Also, the unit tests for the packager were updated to
the new versions of bindings.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Maintenance work continues but this time also one new thing was added to the
console version of the program:
* The program's bookmarks and moving to them.
* Also, added option to enter manualy the destination directory.
* And of course, a lot of fixes for the problems reported by the AdaControl.
* Because static analysis of the program takes some time, I've added a new
  GitHub workflow for it. Thus, everyone can now see how much problems are
  waiting for fix :)

### [Bob](https://www.laeran.pl/repositories/bob)

*Non-Intelligent console assistant (written in Ada)*

Fixing the problems reported by AdaControl slowly moving forward. But this time
even one new thing landed in the code: now when there will be any problem
reported by the program, the program itself will exit with proper exit status.
At this moment it causes problems with unit tests, because it set failure exit
code for passed tests :) Also, some code cleanup was done this week.

