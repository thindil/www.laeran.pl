-- layout: blog
-- title: Weekly development report 2021-08-21
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version is quiet again. Looks like the most annoying bugs are
fixed... or everyone has given up. :) No things to report here.

In the development version, the work on making the game UI more user-friendly
continues:

* Finished work on sorting crafting recipes in the crafting screen.
* Fixed showing tools availability status in the selected crafting recipe info
  dialog.
* Small changes to general UI look, mostly entry fields, like changing the
  ship name, got a bit lighter border to match the look of others UI elements.
* Added sorting to the lists of available recipes to buy, healing wounded crew
  members and repair the player's ship in bases.
* Of course, standard footer here, work with fixing problems reported by the
  AdaControl tool continues. And even got a small boots. :)
* Another thing which can be interested mostly for programmers. To make the
  code a bit less buggy (an optimist, eh) I started using the subset of the
  Ada programming language, called [SPARK](https://en.wikipedia.org/wiki/SPARK_%28programming_language%29).
  Generally speaking, it is a formal verification tool, used mostly in
  high-integrity software, like aircraft or medical equipment. At this moment,
  the work just started, thus there no too much to show. And probably not all
  the code will be possible to verify, due to limits of SPARK. But I hope that
  it will be possible to verify the user interface code. It would be something
  good. Writing normal tests for UI is quite complicated, plus they usually
  can't be run in automated way, mostly because servers don't have enabled
  graphic mode. Formal, mathematical verification of the code, could solve
  this problem. Translation for the players: this should make the game less
  crashes friendly. :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

As promised in the last week. The whole this week was spent on adding various
keysyms supported by the Tk library to `Tk.Bind` package. And here is still
some work to do with it. End of the  report here. :)

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Work on clearing the program code and updating the console version of the
program slowly moves forward:

* Work on merging the same code from graphical and console version of dialog
  with information about the program has started. The graphical version should
  be finished, now focus is in the console version.
* Fixed the script to generate ROOT translation of the project. It wasn't check
  for strings in graphical-only and console-only code.
* Again, one more missing translation string fixed in Polish language.
* Standard, almost copy+pasted from the last weeks: some work with fixing
  problems reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Copy and paste from the previous week: fixing the problems reported by
AdaControl continues. It is still at the `Pages` package. That going very
slowly forward.

### [DockerAda](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

The project documentation got fix for sample commands (how to use images).
Also, Spark 2014 Discovery was added to the adabuild image. The image was
rebuild, and now it needs to be tested. :)

### [Vim-Ada](https://github.com/thindil/vim-ada)

*Ready-to-deploy plugins and configuration which change Vim/NeoVim into (mostly
Ada) IDE*

All things are updated, unneeded patches are removed, the project documentation
updated too. This mean that a new version, [12.0](https://github.com/thindil/vim-ada/releases/tag/v12.0)
is available to download. Due to change to the list of included modules (and
removed some patches for them) it is recommended to check the default
configuration file before update to the new version. And of course, this
project is going sleep again. :)
