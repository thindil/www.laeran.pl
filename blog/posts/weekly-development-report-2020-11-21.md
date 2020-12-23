-- layout: blog
-- title: Weekly development report 2020-11-21
-- filename: blog/posts/weekly-development-report-2020-11-21.html
Welcome to the weekly development report or what was done in my Open Source
projects in the last week. With every week this report is a bit shorter :)

### [Steam Sky](https://thindil.itch.io/steam-sky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version, at this moment is probably the longest period without
bug fixing releases. Which mean that the stable version is really stable. Or
dead :P. Anyway, here are nothing to report.

In the development version of the game the situation with bugs is: oh boy :)
At least, a few of them were fixed this week. Slowly the game back to its
playable state. Furthermore, fun with the game dialog windows continues. This
week wait menu and information about the [player's ship modules](https://imgur.com/YVYKulX)
were done and work on dropping items from the ship cargo started. Also, as
usual, a lot of under the hood work was done too.

### [TASHY2](https://github.com/thindil/tashy2)

*Ada binding to Tcl/Tk, based on TASHY*

Tk Button options can now be also get. Additionally, in Tk.Widget there were
added functions to convert widgets options from String/Tcl_String to their
proper types. Tk.Button package also got some code documentation. Added the
constant Null_Widget to the Tk.Widget package. And in Tcl binding there are
arrived bindings for manipulating Tcl variables (getting, setting and
removing). Also, started work on unit tests for them.

### [Hunter](https://github.com/thindil/hunter)

*Graphical File Manager for Linux (written in Ada)*

The most important information this week: the program finally got it the new
[development release](https://github.com/thindil/hunter/releases/tag/1.5) :)
Before it happened, there were some work on the modules system and added
option to show the first version of the modules documentation in the program.
A few bugs was squashed and the Ada programming syntax highlighting was
updated to the Ada 2012 standard. Also, root and Polish translations of the
program were updated too.

As usual, after the release the first work are done on fixing bugs which
emerged of course one day after the release :)
