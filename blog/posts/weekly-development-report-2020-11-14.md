-- layout: blog
-- title: Weekly development report 2020-11-14
-- filename: blog/posts/weekly-development-report-2020-11-14.html
-- Author: Bartek Jasicki
Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://thindil.itch.io/steam-sky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The saga of playing with the game UI continues:

* Move ship buttons have been reduced a bit, so the last messages window has
now a bit more space.
* A lot of "paper cut" work done: mostly missing keyboard shortcuts but also
some buttons got small lifting to be more visible.
* The most of the week took a rework of various dialog windows in the game.
Previously, they were normal dialogs - with windows decorations and generally
making a mess on a screen. :) The most time was spent on finding a proper way
(read: way which I like the most) to change it. When it was done, finally some
visible work was done too. At this moment only for messages and move map
dialogs. Generally, the main screen of the game looks now [that](https://imgur.com/jCm6uaJ)
(with refreshed move map dialog).
* As also usual, a few bugs were caught and fixed and a few new were
introduced for completion :)

### [TASHY2](https://github.com/thindil/tashy2)

*Ada binding to Tcl/Tk, based on TASHY*

Tk Button now have all its options on the place. At this moment all can be only
set, code for read them from Tcl is not finished yet. Tk.Widget got a lot of
new types to support the options. Also, functions Get_Option were removed and
will be replaced by proper Option_Value functions. Plus, all code which allows
convert widgets options from Ada to Tcl was moved to Tk.Widget package as
Option_Image procedures. Package Tcl.Strings got fix for creating literal Tcl
strings plus new function to convert Tcl_String to normal Ada String. Some the
code documentation was updated, same as the demo program to the newest version
of the library.

### [Hunter](https://github.com/thindil/hunter)

*Graphical File Manager for Linux (written in Ada)*

The work on the program modules is done for now. At this moment the whole
system is a bit simple, but should work by the most time. It should allow
creation of modules not only in Tcl but theoretically in any programming
language. Additionally, there were done some fixes for modules UI. Also, as
an example of module was added Tcl script with allows integrating Hunter with
my other project [Bob](https://github.com/thindil/bob). Also, work on updating
the code documentation was also finished :)

### [Bob](https://github.com/thindil/bob)

*Non-Intelligent console assistant (written in Ada)*

Final work on this version of the program were done and a new, shiny version
3.0 is available for everyone :) Generally in this week Bob got two fixes for
bugs and some code documentation update. A new version is available
[here](https://github.com/thindil/bob/releases/tag/3.0). This mean that this
project going on hiatus again (we will see for how long this time) :)
