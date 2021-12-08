-- layout: default
-- title: Weekly development report 2020-10-31
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html
Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://thindil.itch.io/steam-sky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version - suspicious silence. Which means that I'm blind and I
don't see any obvious bugs :)

In the development version:

* Work on Knowledge screen, the [first version](https://imgur.com/WdS2DRg) is
finished. Funny fact: making the bases list here took one week, making three
others lists another week :)
* A lot of grammar and typos fixed in the project and the game documentation.
Probably a lot more still to fix.
* Under the hood saga with code cleanup and other boring things continues.
* Fixed a few bugs and added a few new for compatibility :P

The most important information - it is again time to release the new
development version of the game. In around 24 hours since this post, it will
be available on the [GitHub](https://github.com/thindil/steamsky/releases)
and (something new) [Itch.io](https://thindil.itch.io/steam-sky). This time
it should be a bit more stable than the previous one :)

### [TASHY2](https://github.com/thindil/tashy2)

*Ada binding to Tcl/Tk, based on TASHY*

Work slowly going forward: added some basic bindings for generic Tk widget and
started work on binding for Tk button widget. Also, some updates to creating
new Tcl commands was done. This was triggered also unit tests and documentation
updates.

### [Hunter](https://github.com/thindil/hunter)

*Graphical File Manager for Linux (written in Ada)*

A few bugs were fixed this week but mostly work is back on the program modules:
at this moment mostly on their UI. It got some small redesign and ability to
start showing available the program modules. And of course, some updates to the
code documentation.

### [Bob](https://github.com/thindil/bob)

*Non-Intelligent console assistant (written in Ada)*

I replaced Travis CI with GitHub actions. The project documentation got some
updates and probably more important, got a lot of grammar and typos
corrections. Also, Bob configuration got some updates: merged unit tests related
commands in one and added command to pretty print the program code.
