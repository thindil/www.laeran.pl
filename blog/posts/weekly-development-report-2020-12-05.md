-- layout: blog
-- title: Weekly development report 2020-12-05
Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://thindil.itch.io/steam-sky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version work on fixing typos is done. At least for now. And of
course, in the last moment, one of the players reported a new bug which was
fixed too. Thus, in less than 24 hours since this post a new, a bit more
stable and grammar correct version of the game will be available for download.

The development version got these same fixes plus generally "paper-cuts" week:

* Dialog which allows assigning crew members to modules got small redesign to
looks like other dialogs. Also fixed keyboard behavior on it (selecting
elements, closing, etc.)
* Fixed scrolling last messages window
* Hide enemy's ship's modules info when combat is finished
* Also, some smaller fixes for other bugs related to the game UI
* As usual, under the hood work on some code refactoring and updating its
  documentation continues

From non-code related thing: the game is now also available on [Game Jolt](https://gamejolt.com/games/steamsky/560699).
[Itch.io](https://Itch.io) is still the main landing page for the game, but we
will see how Game Jolt will help in spreading news about the game :)

### [TASHY2](https://github.com/thindil/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Generally, this week was spent on work on adding bindings for various Tk *grid*
commands. This was triggered also some work in Tk.Widget package (like added
function to convert *Widgets_Array* to Ada *String*). Some code which was earlier
in *Tk.Grid* package was moved to *Tk.Widget*.

### [Hunter](https://github.com/thindil/hunter)

*Graphical File Manager for Linux (written in Ada)*

Almost the whole week dedicated to work with the program translations and their
generating:

* The script to manipulate translations got some fixes.
* Translations strings in the code got updates to remove trailing spaces, etc.
  not needed things from them.
* Both root and Polish translation were updated.
* Also, there was some code refactoring work, like using *TCL_Error* instead of
  exceptions.

I hope that the next week this list will be a bit longer :)
