-- layout: blog
-- title: Weekly development report 2021-09-04
-- filename: blog/posts/weekly-development-report-2021-09-04.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Again, peace and quiet on the Western… err, stable version of the game. :)
Nothing new was found here. I need to dig deeper.

The development version is going in its pace forward. Most of the changes this
week done under-the-hood, not visible and probably not too interesting for the
players (or interesting only as a possible sources of new bugs) :

* Finished work on sorting the list of available items to loot in abandoned
  bases.
* Started work on sorting various lists in the game statistics screen. At this
  moment, only sorting finished crafting orders works.
* The standard task with fixing problems reported by AdaControl continues.
* A lot of work done with trying to prepare the code for formal verification
  of the game. Because I'm new to that thing, it is mostly done with “trials
  and errors” method. A lot of errors. :) Anyway, it is going slowly forward
  and looks like everything works. But sometimes it produces funny results,
  like the game was able to compile in debug mode and not working with release
  and tests. :)

Since the last development version of the game four weeks passed, it is time
for another. In around 24 hours after this post, a new, shiny and probably
buggy development version will be available for download.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The work on adding various keysyms to package `Tk.Bind` is finished. Also,
added a unit test for function `Modifier_Type_Image`. And same as in the
previous week, most of the time was spent on adding ability to use various `Tk`
packages in a SPARK code. The demo program was also updated, so it can be now
ready to test with SPARK. Not everything, but most of the code should be. And
I've added a new subtype `Tk_Path_String` to use it for setting Tk path names
for widgets. It has some dynamic checks, so it should be always proper Tk path
name. Also, the test with a new version of `Tcl.Commands` package was
unsuccessful thus it was reverted to the old version. Only a new subprogram to
convert a Tcl command arguments to list of Tcl_String was added.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Again, due to work on Tashy, in this week, the work on Hunter almost stopped.
Only a few small changes done:

* Fixed refreshing file or directory preview after closing the "about dialog" in
  the console version
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Copy and paste from the previous week: fixing the problems reported by
AdaControl continues. But at least, package `Pages` is ready, and now it is time
for the package `Sitemaps`.

### [TASHY](https://www.laeran.pl/repositories/tashy)

*Ada binding to Tcl/Tk, based on TASH*

The work on making the library, mainly its part related to the Tk binding more
SPARK friendly is done, at least for now. Tashy now should works with SPARK
code. Also, the default compilation flags for the library was changed. The
setup script got option to set linker flags and this mean that Tashy can be now
build as a full console version. The option to automatically create console
only bindings was also added to the setup script. It still needs some tests,
thus it should be finished in the next week. From the work related to the
project organization: Bob command used to push the code to the server uses now
`fossil push` command instead of `fossil sync`. The project documentation got
some small updated either.
