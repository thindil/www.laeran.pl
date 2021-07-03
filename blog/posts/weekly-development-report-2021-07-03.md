-- layout: blog
-- title: Weekly development report 2021-07-03
-- filename: blog/posts/weekly-development-report-2021-07-03.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This week the most visible change in all projects is
update to the new version of Fossil. And all other things are going in their
normal pace.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

As usual, the best day for catching bugs is the next day after a release. :)
Literally one day after the latest stable release, one player reported a
crash. Also, a couple other non-crashing problems were fixed in the game
too. The most visible change will be probably scrollbars. Again, in around
24 hours after this post another, another a bit more stable version will be
available to download.

In the development version, the sage about updating look and feel of User
Interface continues:

* Here also the scrollbars made a bit more visible. After that, I decided
  to play a little with the default theme of the game. The changes are subtle,
  but I think the UI now looks [better](https://imgur.com/Y8QqVwy).
* Started work on some small changes to the game statistics screen. For now,
  it also has fixed scrolling and I changed how the [various lists](https://imgur.com/cBBf3HQ)
  look there. There is some work to do, but it effects shouldn't be that visible.
* The help entry about training skills was updated with some information.
  Also, it now contains a few less typos. :)
* In the trade screen, there is added information about the weight of the items.
  And removed from the list items which cannot be bought or sold.
* In the shipyard screen, the info about required hull size is now more
  descriptive. At least, I hope it is. :)
* In help, there is a new section, at the end of the list, with information
  about all available characters' attributes and skills. Because it is
  possible to add, delete or change every skill or attribute just by modifying
  the game data file, this list is automatically generated at the start of the
  game.
* And of course, the same problems reported in the stable version were fixed
  in the development too. Plus, a couple new bugs were fixed and probably
  introduced.
* Footer as usual: some work in the code was done too. Mostly related to the
  problems reported by AdaControl tool.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The code documentation of the project should now generate without any problems.
I splited the type `Pad_Data` on `Horizontal_Pad_Data` and `Vertical_Pad_Data`
so the setting padding for various widgets will be now a bit more readable.
Field `Grid_Options.Sticky` got its own type instead of just *Tcl_String* thus
it now doesn't require knowledge of Tcl to set it. Of course, all related unit
tests were updated either. Also, there are added some more default values for
various types and a bit more pre and post condition checks.
`Tcl.List.Split_List` function can now also split empty lists now. Earlier it
was crashing when trying to take some widgets default options. Next I started
work on the new version of the library demo program. The old was just an empty
window with one button, the new will be a simple calculator. At this moment it
is a work in progress stage. The basic UI is on its place, now I need to add
the whole code to calculate everything. :)

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week, as a few previous, was almost complete copy of the previous week:

* Continue work on setting the user defined commands in console. Now it is
  possible to add a new command or edit existing. There is still to do deleting
  them, but that should be done fast.
* Added linking time optimization option to the program's compilation flags.
  It should build a bit faster executables.
* All checks, like pre- and post- conditions, etc. are moved to the debug only
  builds. This also should speed a little the program.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Same as with the Hunter, the whole report could be copied from the previous
week. And this means: AdaControl still reports problems in the `Config` package.
Thus, the whole week was spent here on fixing them. And same as in the project
above, I added linking time optimization option to compilers flags when build
the stable version of the program. Also, all additional checks like pre- and
post- conditions are moved to the debug builds only. Some cleanup in the Bob
commands related to the project was made too. And now the work started on
adding some more contract based programming to the project.
