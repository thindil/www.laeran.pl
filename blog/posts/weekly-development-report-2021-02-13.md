-- layout: blog
-- title: Weekly development report 2021-02-13
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

This slowly is starting to be a tradition: when I find one bug in the stable
version, almost always the second appears somewhere too :) Which mean, in
around 24 hours since this post, a new bit more stable version of the game
will be available for download.

In the development version of course, work on the UI slowly moving forward,
almost as usual:

* Generally, some elements of UI, like small and switch buttons now looks more
like 3D elements. It is probably the best visible on the new game screen,
[the last week](https://imgur.com/ljMCvT5) version and [this week](https://imgur.com/gy1pOVG)
version. Also, there were a few small fixes to various UI elements (like map
info frame).
* Most of the buttons and other UI elements in the main menu got tooltips,
they should be more new player friendly now.
* Bugs from the stable version were fixed here too.
* A small thing, but I'm happy how it works: the looting, the shipyard and the
hiring recruits screens now have a more consistent [look](https://imgur.com/9dYvdLV).
There is still some work to do, but I like how it looks and works.
* And as usual, some work more interesting only for programmers: some code
documentation updates and the code itself got a few cleanups.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Work on `Tcl.Lists` package is finished for now. It can convert the selected
Tcl list as variable name or just plain list to Ada arrays. Also, a few more
general bindings and auxilary subprograms for manipulate various `Ttk_Widget`
options were added too. As usual, during adding unit tests for them, a few bugs
emerged too :) They are fixed also. `Ttk_Button` got some missing options
update. And started work on `Ttk_Label` package. The binding is almost
complete, now it need only to write some unit tests.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week brings a bit more options to the console version of the program:
* Fixed showing messages during creating files and direcotries
* Added ability to rename files and directories
* Most of work in this week was related to the option to copy selected files
  and directories. For now, simple copying without overwritting should works,
  here are still some work to do with handling messages during copying.
* Also, some small code cleanup and optimization were done.

### [Bob](https://www.laeran.pl/repositories/bob)

*Non-Intelligent console assistant (written in Ada)*

Bob got another build-in command: show which allow to preview setting for the
selected local command. It shows variables and their values, commands to
execute and flags related to the selected Bob command. That is probably the
last thing which will be added to the Bob, now the maintenace work started:
some small code refactoring and beautyfication. Also, added rules for
AdaControl for force some coding standard (on myself, eh). In the next week
probably there will be a lot of changes to the code :)
