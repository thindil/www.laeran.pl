-- layout: blog
-- title: Weekly development report 2021-01-30
-- filename: blog/posts/weekly-development-report-2021-01-30.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

\[Copy + paste info about fun with UI in the development version\] as usual :)

* Updated shipyard UI a bit: removed the old selection of install or remove
modules with the new [buttons](https://imgur.com/V2rWUox).
* I'm a bit surprised, but I was able in this week to do the whole redesign of
[loot screen](https://imgur.com/C27fip5). Of course, there is still a lot of
room to improvement, but the main design of the whole game UI is finished. Now
it is time for work on something what I call "paper-cuts": thousands of small
tweaks, fixes etc. things in various places which pretty often made the UI very
annoying or unfriendly. This mean that I should finish (mostly) work before
the next major stable release :)
* Code as usual, got some cleanup and its documentation was updated. At least
I should know now what most of the code is doing :P
* And as always, right after the release I found a few bugs. They are fixed
thus, there is now again some space to add a few new.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Work on the code documentation for the package `Tk.Menu` finally is finished.
Also, all unit tests related to the package are on their places. During the
work, some bindings were changed a bit: mostly replaced some menu entries
indexes `String` parameters with `Tcl_Strings`. A few bindings related to the
manipulation of menu entries got overloaded bindings with ability to set
indexes as proper enumeration `Menu_Entries_Indexes` or numeric values without
need to convert them. Work on package `Tk.TtkWidget` was also started this
week, and almost finished either.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Now console version of the Hunter slowly starts looks like a file manager :)
* Added option to create files and directories
* Added UI to delete the selected items
* Added deleting the selected items from the current directory
* Fixed selection of multiple files and directories in the current directory
* Fixed crash on entering to the empty directory
* And started some cleanup work on the program's translations strings

### [Ada-Bundle](https://github.com/thindil/Ada-Bundle)

*Maintained complete Ada-Mode for Vim/NeoVim*

This week brings only small changes to the project: removed support for
non-existing plugin Ada-Spec added command to set additional options for the
compiler (like `-XMode=release` or flags for binder) and updated the plugin
documentation (with some grammar and typo fixed). And the project is going to
sleep for now again.

### [Vim-Ada](https://github.com/thindil/vim-ada)

*Ready-to-deploy plugins and configuration which change Vim/NeoVim into (mostly
Ada) IDE*

Big changes and big event: a new version of the project is [released](https://github.com/thindil/vim-ada/releases/tag/v11.0).
Additionally, to changes from the previous week, it brings updated the Vim/NeoVim
configuration for the Ale plugin and fixed patch for the Vim-header plugin.
Also, plugins Fugitive and GitGutter were removed. This last was replaced by
Signify (which works with more version control systems). A new plugin,
Grammarous was added to the project. The project documentation was updated to
the new list of plugins too. Also, the project help file should be now more
grammar friendly. And same as Ada-Bundle, this project also going for sleep for
now.
