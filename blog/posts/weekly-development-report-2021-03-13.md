-- layout: default
-- title: Weekly development report 2021-03-13
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. Same as the previous week, the most of the week (in
some projects even all) was spent on work related to the static code analysis
and fixing problems reported by it. Now a bit more details.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And traditionally, the previous week was with screenshots, this one must be
without :)

The week was spent on various under the hood works:

* Fixed hiding next turn button in combat after win it in boarding
* Boarding combat UI got some small polishing
* Fixed some other bugs related to the combat and its UI
* Started work on updating the knowledge screen. The bases list got redesign,
now it should work faster and also load faster. Additionally, it got
information about the player reputation level in the visited bases. Some small
clarification in the selected base info was done too
* A lot of code cleanups and refactoring were done too. Also, the unit tests
were updated.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

As in the previous report: fixing problems reported by AdaControl continues.
`Tk.TtkLabel` package now should be ok. Same as packages `Tk.MainWindow`,
`Tk.Toplevel` and `Tk.Button`. The work started currently on `Tk.Menu` package
but it is also almost finished. Additionally, the unit tests for the packages
mentioned above were updated to their new versions.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Another week spent almost completely on various maintenance tasks. But, in the
console version of the program there is some new things too:
* Fixed some bugs in console version related to the program's bookmarks.
* Also in the console version, added option to create symbolic links.
* A lot of work with fixing problems reported by the AdaControl. But this work
  is still closer to start than to the end.

### [Bob](https://www.laeran.pl/repositories/bob)

*Non-Intelligent console assistant (written in Ada)*

Same as in previous week(s): fixing the problems reported by AdaControl is
slowly moving forward. Also, the program's unit tests were fixed so, here
everything back to normal :) Also, GitHub workflow was updated to the new
version of the code, thus at least this one thing is done.
