-- layout: default
-- title: Weekly development report 2021-01-23
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This time the report contains a bit more entries
than usual.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And fun with redesign UI in the development version, as usual, continues.
To be honest in this week was done even a bit more than I expected :)

* The first version of new UI to hire new crew members in bases is
  [done](https://imgur.com/UVmy5Ge). Now these dialogs literally cry for some
  headers :) Soon™ they should be added (read: before the development version
  will be the stable version).
* Also started and almost finished work on a new version of the
  [shipyard UI](https://imgur.com/i1JgQMC). Here is still some work to do yet,
  but also soon (the next week?) should be finished.
* Some small changes to UI are done too, like for example, looking for a module
  to install is now case-insensitive, some padding between UI elements, etc.
* Under the hood again the code documentation was updated plus some minor code
  cleanup/refactoring.

And the most important information this week. It is time for share all these
new bu... features with the world. In around 24 hours since this post a new,
shiny development version will be available to download everywhere :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

And unit tests for the Tcl.Info package are on their proper places. Same for
unit test for Tk.Main_Window package. The most of the work in this week was done in
creating binding for Tk widget menu. It is almost done now. The bindings are on
their places, also some simple unit tests were added for them. Now only to
write documentation for it and add a few missing tests. As usual, tests
detected some problems with bindings and the problems were fixed too.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Work on console version of the program is slowly going forward:
* Default shortcut for quit from the program was changed to Alt-Q. Also, the
  menu for quit works.
* Added very simple for now preview of the selected items: only directories and
  text files. Text files if they are source code have same syntax
  highligthning like in the GUI version. At this moment, text file preview
  works only with the beginning of the files.
* Started work on actions' menu, for now only for creating directories and files
* As always, some under the hood work: mostly related to the code documentation
  were done too.

### [Ada-Bundle](https://github.com/thindil/Ada-Bundle)

*Maintained complete Ada-Mode for Vim/NeoVim*

Here only one change, but may be a bit breaking: updated the support for Ale
plugin to its newest version (which finally supports officialy Ada, yay).
This mean that Ada doesn't require any more additional plugin vim-ada to have
working support for Ada Language Server. At this moment I don't have plans to
move this project to a Fossil repository. The main reasons are that:
* This project is rather rarely updated and
* It is required to have Git version of the project so anyone can their
  favourite Vim/NeoVim package manager to install it easily.

### [Vim-Ada](https://github.com/thindil/vim-ada)

*Ready-to-deploy plugins and configuration which change Vim/NeoVim into (mostly
Ada) IDE*

Same as above, only one change to the plugin but also breaking: updated to the
newest version (for this same reason as above) of Ale plugin. But here will be
some work in the next week. And as same as above, at this moment there are no
plans to move this project to the Fossil.
