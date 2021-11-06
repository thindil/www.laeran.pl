-- layout: blog
-- title: Weekly development report 2021-02-06
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And as promised, the whole week was related to fixing and making small changes
to the game UI.

* Finally, the shipyard screen shows real prices, based on trader skill and
the player reputation, for ship's modules. Also, it got some other small
changes and now [looks that](https://imgur.com/u0l0wI8).
* Also, as visible on the screenshot above, I've started work on the general
UI update, to make it less flat and more in "retro-futuristic" style. At this
moment it is still mostly fun with colors to made UI elements to look like 3D,
but probably in the distant future I finally do any nice images for it :)
* The new game menu got also some small updates (mostly elements got some
spaces between them). And [here](https://imgur.com/ljMCvT5) probably are the
most visible changes which were made to the UI. A few elements still need
some work (for example the small buttons) but at least it starts looking a bit
more interesting :)
* Also, some small fixes to the UI in various places were done.
* Under the hood, the real never-ending story with small updates to the code
and its documentation continues as usual.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The base work on package `Tk.TtkWidget` is almost finished (same as earlier
week :)). Added some unit tests there and started work on package
`Tk.TtkButton`. During this work turned out that there is a need for some more
work for various `Tk.TtkWidget` bindings. The most of them are added now. Also,
Tcl binding got Ada version of `Tcl_SplitList` to convert Tcl lists to Ada
arrays. The work on it is almost finished too, just need to add some unit
tests. And the project documentation got some updates: mostly some
clarifications.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The most work of this week was maintenace work:
* Removed new line character from all translations strings
* Updated ROOT and Polish translations to the new version of texts
* Updated the project documentation, mostly contributing guide, other
  documentation got mostly formatting work
* Started work on showing error messages during creation of new items

### [Bob](https://www.laeran.pl/repositories/bob)

*Non-Intelligent console assistant (written in Ada)*

Special guest this week. The project wasn't touched by few months, thus now it
is some time to refresh it :) The main change is it new home is now [Fossil](https://www.laeran.pl/repositories/bob)
too. The old [GitHub repository](https://github.com/thindil/bob)
will still be updated but the whole development and support will be moved to
Fossil. Added another mirror of the repository on [GitLab](https://gitlab.com/thindil/bob).
This one is fully automated. This week work was related to fun with runnig the
Bob inside [Valgrind](https://www.valgrind.org/). One bug was found and crazy,
100 bytes memory leaks were fixed too. Generally, this project is almost
finished, thus the most of the work now will be related to the code
optimization and cleanup.
