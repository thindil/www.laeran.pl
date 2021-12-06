-- layout: default
-- title: Weekly development report 2021-07-24
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Stable version in this week was quiet. Which means, as usual, I probably miss
something there. :)

In the development version, the fun with UI continues:

* The most of the week spend on adding ability to sort various lists in the
  game. As always, it started slowly but after finished the first list, the
  work got some speed. For now, it is possible only to sort saved games and
  player ship [info lists](https://i.imgur.com/a1XIGHb.mp4) (like modules,
  crew and cargo). Nothing big, but after all I really like this feature,
  especially in later game, with many items in cargo or big crew.
* The work on sorting the crew members inventories started. Here is one more
  problem to solve: sorting items by usage status (used or not) before it will
  be finished.
* Under the hood, as usual, some problems reported by AdaControl tool were
  fixed. Also, I added a few more unit tests and fixed code documentation for
  a few subprograms.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

As promised, this week report is very similar to the previous week. :) The work
on `Tk.Winfo` package as bindings for various Tk **winfo** commands is almost
finished. All the bindings are on their place, also unit tests for them are
added. Now started probably the longest and the most boring stage: adding the
code documentation.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The work on the console version of the program (at least it's the first alpha
version) is slowly ending. There left only a few things to do and let's hope in
the next week, there will be finally a new release of the project. For now, in
this week were done:

* Work on showing content of the system Trash is done. Now it is possible to
  see everything what is in the Trash and navigate around in the console
  version.
* The main program menu in console got its special version when showing Trash.
  It still needs some polishing but for now it works as expected.
* Added restoring items from Trash in the console version of the program.
* During some work I changed how selected items are stored in the console
  version. The effect was that the program stopped moving, copying or deleting
  files and directories. Now all of these actions works again.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

As usual, quite short report here: fixing the problems reported by AdaControl
static analyzer continues. At this moment I'm at `Modules` package, thus most
of the code should be fixed. Work on adding the unit tests to the project
continues. I added now tests for loading the program modules and various tests
related to create the Atom feed for websites.
