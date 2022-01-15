-- layout: default
-- title: Weekly development report 2022-01-15
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. The first week without any changes to the
development tools. But the general work on the projects is very similar to the
previous week. One of the most visible changes, is that some projects
(AdaPlanet, AdaSearch and Bob) are archived on GitHub and GitLab now and
removed from Fossil, the reason: I don't work and don't plant to work anymore
on them.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The third week of the preparation for the next big stable release passed.
This time even less to show than earlier. But there are some changes in the
game's code, technobabble below:

* A lot of work done with clearing the game's code and generally bringing some
  consistency to it. Same as previous week, changes triggered some updates to
  the unit tests.
* Some preparations for formal verification of the code done either. This work
  triggered a few large changes in the code. It looks like it not created any
  new bugs, I hope. :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This time copy and paste from the previous week, removed again a few things. :P
The whole week spent on fixing the problems reported by gnatprove. The work is
slowly moving forward here.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous week. Thus, almost the same
report as the earlier:

* Clearing the code of the console version of the program slowly moves forward.
  All dialogs should now use the same code for creation. The work started now
  on merging the code related to the moving around the dialogs fields.
* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. Removed here the last line, so some things are
  changed. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The most changes in this week are in the project. The shell is in the shape
which allows using it as a replacement for the previous project, Bob. At least
it is used during development of itself. :)

* The base work on the shell aliases is done for now. It is possible to list,
  delete them or to show their content. The rest of the commands related to
  aliases should be added soon(TM).
* The in-program help upgraded with information about the new available
  commands.
* Fixed entering directories. Now it goes to the real directory, not its
  symlink.
* The project's documentation updated with information about the shell's
  aliases.
* Better the shell's history. It is now saved in the database, thus is
  persistent between sessions. It is still a very simple history system, which
  need a lot of work.
* The changes in the code triggered again some code refactoring and cleanup.
* Fixed adding `exit` command to the shell's history.
