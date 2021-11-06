-- layout: blog
-- title: Weekly development report 2021-01-09
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.


### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Again, the stable version is stable... or at least looks stable to me. And
probably as usual I'm wrong :P
In the development version, the almost never-ending saga of updating UI
continues.
* Finished work on the new look of trade. Of course, as usual, each solution
causes new problems. I'm start thinking when I'm looking on this screenshot
that dialogs need some more visible borders. This one is blending in
background for me.
* Crafting UI, statistics UI, school UI and last messages UI also got some
small fixes and improvements. They probably will be changed later to looks
similar like others.
* Started work on updating UI for buying recipes, repair ship and healing
crew members in the bases.
* A few changes to made UI a bit more user-friendly. For example, when you
enter a too big numeric value into an entry field, it will be changed to max
allowed value.
* As usual, a few bugs were fixed probably by covering them with new bugs :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The main change to the project setting was enabling all checks (not just
preconditions). Also, fun with unit tests continues. Tk.Button has all
subprograms tested a bit and work started on package Tk.Grid unit tests. As
usual, a few bugs emerged during the test phase, thus they were fixed too (some
even related to the conversion Strings from Tcl to Ada). No new binding were
added this week.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Work on the console version of the program slowly moving forward. At this
moment the main program window is almost done: added the main menu, path
buttons for the current directory listing and the listing itself. It is
possible to select item on the listing and work started on showing preview or
info about the selected item. Also, fixed showing preview of empty directories
in graphical version of the program. From the standard, code cleanup work: a
few loops got labels and some small code refactoring were done too.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

Here only some small changes, invisible for the visitors:
* Removed from templates summary element
* Added description meta tag to the pages

That is all for some time. The next big update (not counting new
blog's entries of course) probably in a few months. At this moment this project
is going sleep. :)
