-- layout: default
-- title: Weekly development report 2021-01-16
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This time publication is a bit plagued with network
problems.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Saga with updating UI continues. At least in the development version. Because
the stable version is quiet as almost usual :) And more details:
* Search for recipes to buy in bases is made case-insensitive
* Small updates to UI for buying recipes, healing wounded and repair ship in
  bases
* Updated UI for available missions in bases (especially reward setting now
  should be a bit more user-friendly)
* Started another big work on UI: redesign UI for hiring recruits in bases.
  I want to test one concept of UI here. If it works, I will implement it
  also in other places in the game. At this moment it is in the middle of task,
  thus no screenshots this week. This is almost tradition too :)
* Some code cleanups and refactoring are done too.
* A few bugs were fixed and let's hope a few less added to the game :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Added a unit tests for the Tk.Grid package. Of course, they detected some
problems with bindings, which were fixed too. The main work in this week was on
adding bindings for various subcommands related to the Tcl command `info`. This
is done as package Tcl.Info and at the end of the week I started work on adding
unit tests for them.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Almost the whole week was spent on adding showing preview of the selected
directories and text files. At this moment it is a very simple preview,
especially for files: it shows only beginning of them. Also, a few bugs in the
console version of the program were fixed (for example, moving between windows
with Tab key). As typical footer for this section: a few loops got labels and
some small code refactoring were done too.
