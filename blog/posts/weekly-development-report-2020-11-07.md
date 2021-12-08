-- layout: default
-- title: Weekly development report 2020-11-07
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html
Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://thindil.itch.io/steam-sky)

*Roguelike in a sky with steampunk theme (written in Ada)*

After the new release of the development version, as usual, the week started
with fixing bugs (and adding changes suggested by people in the previous week
:)) Then, I back to the almost never-ending saga of tweaking the game UI.

* The most visible change this week is the style of information about the ship
in the right up corner of the UI. Earlier, there was always info, even when
everything was ok. Additionally, every of this information was button to the
proper information screen. Now, when almost everything is in the same place,
there is no need to have that option, especially that it just double the
existing menu entries. So, it was replaced by [standard colorful labels](https://imgur.com/gF1aA8m).
Also, now it shows only needed information (like on the screenshot: lack of
gunner and crafting on the way).
* The small buttons got a little tweak, so they are a bit better recognizable
as buttons. Should be visible on the screenshot too.
* Information dialogs (like messages or  items information) got some changes
too. For example, messages show the countdown timer to auto hide.

### [TASHY2](https://github.com/thindil/tashy2)

*Ada binding to Tcl/Tk, based on TASHY*

Added package Tcl.Strings. Even if Tcl has only one type of variables, it
strings can be literal or to evaluation. To make things a bit easier, I've added
a new type of string which automatically convert and escape the proper signs
when converted from Ada code to Tcl. Function Tcl_GetStringResult was replaced
by Tcl_GetResult functions which return a Tcl results in a few types. Also,
various Tk bindings got updates in this week: mostly work on Tk Button widget
slowly going forward. Plus the library unit tests and the demo program were
updated to the newest version of the library.

### [Hunter](https://github.com/thindil/hunter)

*Graphical File Manager for Linux (written in Ada)*

Work on the program modules continue. Added option to show the selected module
content and added option to enable or disable the selected modules. Also, the
modules got some triggers like on start or quit from the program. From the
invisible part: the work on updating the code documentation continues.

### [Bob](https://github.com/thindil/bob)

*Non-Intelligent console assistant (written in Ada)*

Finally, some new things here :) First it is now possible to set if
path in commands to execute is typical for Windows or for Unix systems. In that
situation, when the command is running on different system, the path is
translated if needed. Also, command to entering the directories got some small
updates. The second new thing this week is build-in command to convert any file
to the Bob configuration file. If the program configuration file exists, this
command just add the content of the selected file to the existing
configuration. Additionally, was fixed crash on invalid entry in a
configuration file. Plus the program got some small code refactoring work under
the hood.
