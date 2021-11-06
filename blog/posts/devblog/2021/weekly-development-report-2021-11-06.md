-- layout: blog
-- title: Weekly development report 2021-11-06
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another quiet week in the stable version. As usual, I'm probably missing some
bugs. Well, soon, or later I will find them… or someone helps me with them. :)

In the development version, the work on various in-game menus continues:

* The main in-game menu finished for now. It look-and-feel didn't change since
  the last week, but now the “Help” option shows the proper help topics
  depending on what screen is currently visible (like trading help on trading
  screen, etc.).
* The menu to manipulate saved games [updated](https://imgur.com/fjug7jI) too.
  This took the most time in this week, but the code used  here is now almost
  “template” for the other menus for various lists in the game.
* The crafting, player's ship's crew members' inventory and cargo, recruit's,
  known event's actions menus also updated to look similar to the saved game's
  menu.
* Fixed showing the proper event on the map when selecting it from the list of
  known events.
* Added name of the crafting recipe to the dialog header when showing
  information about the selected recipe.
* As usual, under the hood some work on code cleanup and its beautification.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

As the work on making the code better continues, I decided replace the current
setting for colors for various Tk widget from string (exactly `Tcl_String`) to
new, special type. This caused to create a new package `Tk.Colors`. The work
here just started so, not too much done. Before it started I finished changing
Create subprograms preconditions for various Tk widgets. It again moved various
`Options_To_String` functions to packages' specifications and adding unit tests
for them. The functions `Tcl_Get_Result` for returning result as Integer or
Float changed their returned values to `Tcl_Integer_Result` and
`Tcl_Float_Result` respectively. This allows to return also information if
conversion was successful and if not, the message with information what goes
wrong. Another big change this week is set the maximum length for the Tk
widgets path names and Tk image identifier. It is now set to 4096 characters.
It is still very high limit I think, but should be absolutely enough. This
change had pretty large impact on the gnatprove result. It helped to prove
around 200 various checks. :) And it should also later reduce needed amount of
various pre- and post- conditions in the code. As usual, during the work, a few
new problems reported by AdaControl tool fixed too. Which was now added to the
standard tests of the library.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The week of beautification of the console version. That could summarize the
most of changes in this week:

* Now it is better visible which element of UI is selected in the console
  version of the program. Menus and path buttons are highlighted when they
  have a keyboard focus. Views, like the current or destination directory
  now have frame around only when they are an active element of UI. There is still
  some work to do with it, but I hope to finish it in the next week.
* Scrolling the list of files and directories in preview window in the console
  version is fixed now.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

The whole week took some small work to update the project to the newest version
of [YASS](https://www.laeran.pl/repositories/yass). It means mostly removing
unneeded settings from various pages. Nothing visible for humans, only spiders
have now some work to do either.
