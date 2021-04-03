-- layout: blog
-- title: Weekly development report 2021-04-03
-- filename: blog/posts/weekly-development-report-2021-04-03.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This week has list of projects a bit longer than
usual.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Final countdown to the next major version release continues. The most of this
week report could be copied from the last week :) Anyway:

* Adding pagination to various lists in the game goes on. In this week got it:
accepted missions in knowledge screen, shipyard available and installed
modules, items in trade screen, the player's ship's cargo and crew. The most
time took adding pagination to the shipyard. After this, the others were
almost the favorite programmers' technique: copy+paste :)
* Fixed a few bugs related to the trade screen, accepting and generating
missions in the bases. Also, the game finally remembers the position of the
last messages window correctly. This one bug was a good example that sometimes
something what looks like easy to do isn't that easy :) Generally it was
required more changes to code that fixing the others. The GUI code definitely
needs cleanup.
* Constant work on fixing problems reported by static analysis, mostly related
to the code standards continues.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Code refactoring continues. The library no longer need `GNAT.Split_String`
package. It was replaced by own `Tcl.Lists` to convert various Tcl list results
to Ada arrays. Added `Execute_Widget_Command` function which returns String,
mostly for reduce code needed for some Tk commands which returns values. Also,
added generic functions which convert that results to Ada scalar or float
values. And then I've started using the new functions in the code :) That same
was done for `Tk.Button.Invoke` functions. Now is only one which returns String
and two generic which allow better tunning it returns value conversion. Due to
these changes, the project's unit tests were updated either. And started work
on bindings for Tk command **wm** in `Tk.Wm` package.

From the other things, the library now can be automatically build in *headless*
mode: at this moment it means build only binding for Tcl no Tk.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Again, very small amount of work done here, only maintenance mode:

* Generally, a lot of work with fixing problems reported by the AdaControl. This
  was almost all what was done this week in the project.
* Fixed problems with reseting selection when deleting items and refreshing the
  preview after it.
* Possible crash during auto-refresh directory view was fixed too

### [Bob](https://www.laeran.pl/repositories/bob)

*Non-Intelligent console assistant (written in Ada)*

And here work is done, the new version were [released](https://www.laeran.pl/repositories/bob/wiki?name=Download).
The last thing done (for now) in the project was adding build Raspberry Pi
version of the program to GitHub action. And switched to the other projects :)


### [Docker Ada](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

Special guest this week. This time it got some small fixes of typos in the
available images list, but also the new image: adabuildraspi. It is generally
GNAT FSF image for armv7 with added Tcl. Adabuild and Adabuildwin64 images got
updated plus they have new libraries installed on self: libcmark and libaws.

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

This is a real necromancy :) The project was revived after more than one year
of hiatus. The biggest change this week was move the development code of project
to the new [Fossil](https://www.laeran.pl/repositories/yass) home. This
conversion was done without problems, mostly because structure of the project
is very simple, compared to Hunter or Steam Sky. Everything is now in it new
home and there are available mirrors on [GitHub](https://github.com/yet-another-static-site-generator/yass)
and on [GitLab](https://gitlab.com/thindil/yass). This one is fully
automated. Generally, the whole week was related to the moving the project
documentation to the Fossil. Some small changes like updated configuration for
ROBODoc and updated the project README.md file were done too.
