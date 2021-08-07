-- layout: blog
-- title: Weekly development report 2021-08-07
-- filename: blog/posts/weekly-development-report-2021-08-07.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And again, suspiciously quiet week in the stable version. There must be bugs,
just I can't find them. :) Well, probably soon, or later I will catch any,
especially if someone will show me them.

In the development version, the work going as usual:

* The whole knowledge screen lists got option to sort them in various ways.
  The longest part was adding sorting to the list of known bases. The first
  reason: it is a bit long list, the second there are several options to sort
  it. Anyway, work on it is now finished, same as sorting for known events and
  accepted missions.
* The work on the sorting items in trading screen (for bases and traders) are
  started. For now, only sorting by name and types are done. Plus still, items
  from the player ship cargo are shown as first, before items available only
  in base or trader cargo.
* The work on updating the debug window also moves forward. The most of the UI
  are updated, only adding or deleting in-game events are still in need of some
  work.
* As usual, some work under-the-hood with generally making the code better
  looking and working. Plus fixing bugs.

As another four weeks passed since the last development release, it is time
for the next. :) In around 24 hours since this post, it will be available to
download.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The work on `Tk.TtkEntry` package continues. All bindings for **ttk::entry**
widget commands are added now, same as unit tests for them. The code was also
checked with AdaControl, thus should look good (literally). Now the worst
work before me: adding the code documentation to the package. :)

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

As usual, the hope is mother of stupid. :) Again, due to some work on the
project, the new release is postponed to the next week. This week the list is a
bit short:

* Added deleting items from the system Trash in the console version of the
  program.
* Fixed showing items paths when deleting them from the system Trash in console
  version.
* Fixed refreshing items preview after back to the program from its options in
  the console version.
* Fixed refreshing items preview after deleting item from the system Trash in
  the console version.
* A lot of fixes for the code documentation.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Again and again: fixing the problems reported by AdaControl continues. Now it
is at the `Pages` package. The work on adding the unit tests to the project
is finished for now. I've started now some code refactoring tasks. During them,
I found, that setting the site description when creating a new project in
the interactive mode not works correctly. It is fixed now.
