-- layout: blog
-- title: Weekly development report 2021-02-20
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version again entered into sleep mode. Nothing new here.

The development version work continues as usual. On topic as usual either. :)
Visible changes are:

* I've added some tooltips to various UI elements with short explanations. It
isn't that good like tutorial, but should help new players to find self in the
game.
* I found the last dialog which was still done as a separated window. Hunted
it down and rewrote it, so now it looks like other dialogs.
* The trade with bases screen got [redesign](https://imgur.com/jsFlY5R) in
style of the shipyard screen.
* Also started work on redesign ship info screen. It is almost finished, just
cargo info is still in old style.
* As usual, a few bugs were found and fixed. The bugs' amount added to the
game in this week is unknown :)

Things under the hood:

* Continues work on code cleanup and documenting it.
* I've decided to finally add some more advanced coding style to the game.
Until now, it was very loose "standard", probably only line length was really
checked. I've used to do it build-in features of GNAT, the Ada compiler. And I
must say, it was a very time-consuming idea. I expected some warnings but not
that much :) Anyway, this week was spent also on bringing some civilization to
the game's code.
* Also, inside the code, I've started some preparation for another big thing
which I want to add to the development process of the game.

And the last thing today, probably the most important: since the last
development release has passed 4 weeks, thus now it is time for the next.
Thus, in less than 24 hours since this post, a new, shining from bugs version
of the game will be available to download :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The first part of the week was dedicated to testing and fixing all the newly
added bindings to various `Tk` `ttk` widgets. But now everything should work
properly. The second part of the week was spent on adding static code analysis
to the project. I'm using [AdaControl](https://www.adalog.fr/en/adacontrol.html)
for it. There were some problems at the beginning to set it properly to work,
but now it works. And report a lot of problems with code :) At this moment,
only `Tcl` package should be fully checked. It also gains a new procedure
`Set_Interpreter` to change the current default Tcl interpreter. The static
analysis now started on `Tcl.Lists` package.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Work on the console version of the program slowly moving forward:

* Finished work on copying files and directories. Or at least it looks like
  finished. It needs some tests thus probably in the next week here will be some
  fixes.
* Added option to move files and directories.
* Added info about files and directories sizes to the directory view
* Same as in Steam Sky, I've added style checking to the project and started
  fixing all problems reported by it. Here work should be finished for now.

### [Bob](https://www.laeran.pl/repositories/bob)

*Non-Intelligent console assistant (written in Ada)*

As the maintenance work continue here, the whole week was related to running
static code analysis and fixing all reported problems. It still has a lot of
things to do, thus probably a few next weeks will have that same content of
weekly reports :)

### [Docker Ada](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

This week special guest, with only one change: AdaBuild image got AdaControl
package inside. Documentation were updated, same as the Docker image.
