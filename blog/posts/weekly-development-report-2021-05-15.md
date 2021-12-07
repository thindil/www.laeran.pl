-- layout: default
-- title: Weekly development report 2021-05-15
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This week I finally upgraded my Kubuntu to 21.04.
This caused to upgrade the whole development toolchain too. Some things started
working better, some stopped. :) Also, it required some changes in the projects
too. More details are below.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The preparation for the stable release was a bit more interesting than usual.
Literally a few minutes before, I found a few crashing bugs. Probably, the
best moment for it. :) They are fixed now. Anyway, since then no new bugs
reported or found. I need to investigate it.

In the development version, work as usual:

* The same bugs found in the stable version were fixed too.
* Raised possible duration for ship's events when setting them in the debug
  menu.
* Finished work on scrolling UI's elements with mouse wheel.
* Started work on adding headers to the various dialogs in the game. It isn't
  finished yet, thus for now, no screenshots here.
* As usual, some work with code cleanup and refactoring were done too. Let's
  hope it doesn't introduce too much new bugs to the game. :)

And probably the most important thing: it is time for the first development
release of the 7.0 series. This one will be a very interesting release: the
first one which will not use AppImage on Linux or installer for Windows. Just
plain archives: unpack and run. It will be available to download in around 24
hours since this post.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Almost the whole week was dedicated to writing the code documentation for the
`Tk.Wm` package. There is still some work to do, but generally it is almost
finished. Additionally, the parameters for subprograms `Max_Size` and
`Min_Size` were changed. As usual, after that the proper unit tests were
updated too. New binding, for Tcl command **update** with own unit test was
added. The problem with getting Integer value with `Option_Value` function with
entered empty value was fixed too. And as mentioned at the start of the report:
some work required to update the project to the newer version of Tcl/Tk and
GNAT were done too.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week brings only one visible change to the project:

* Added option to run the selected file or directory with the selected command
  in the console version of the program.
* Same as in the other projects: some work on update the project setting to the
  new version of toolchain were done too.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl.

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

As usual, work on fixing the problems reported by AdaControl slowly moves
forward. But this week brings also a new thing to the project: it can now
automatically create canonical links for pages. It is also possible to manually
set them. The default generated page has now documentation how to set it.
Additionally, the project documentation was updated with information
how to build the project with Docker images. And same as above, updated the
project to the new version of development tools.

### [Docker Ada](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

One important change to the AdaBuild image: now libxmlada libraries are set to
be statically linked when build something. Also, the image description in the
project documentation was updated too.
