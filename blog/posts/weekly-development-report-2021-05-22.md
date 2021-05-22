-- layout: blog
-- title: Weekly development report 2021-05-22
-- filename: blog/posts/weekly-development-report-2021-05-22.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. After changes to the development toolchain in last
week, this one is a bit quieter.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

When I was thinking that this week will be quiet in the stable version, the
reality was informed me today that I'm wrong. :) I found a few typos in the
stable version. They are fixed now, but I will take one more week to check
a few things before another, a bit more stable version will be released.

In the development version, wheels keep slowly turning ahead:

* Finished work on headers for in-game [dialogs](https://imgur.com/8OMim2R).
  I think it looks a bit better than the [old version](https://imgur.com/jatvADP).
  Generally, the whole code of dialogs need to some cleanup and that should be
  done in the next week.
* Fixed the same typos which were found in the stable version.
* Some work on the project organization, mostly related to the code tests. It was
  the effect of updating the whole working tool chain to the newer version.
* As usual, fun with code cleanup and refactoring slowly moving forward.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Work at the `Tk.Wm` package is finished for now. Most subprograms were
renamed to better reflect their functionality. Most functions got prefix
`Get_` and procedures got prefix `Set_` to their names. Also, the code
documentation was updated: enumerations got more information what each value
mean and subprograms got information about proper Tcl commands related to them.
And of course, the unit tests for the package were updated to the newest
version too. The same work currently started for the `Tcl.Info` package. Other
things done this week: a new binding for Tcl command **update** was added. In the
project organization: the AdaControl checks were moved to the separated GitHub
workflow. It should trigger that same as the default but, due to some problems
with GNAT 10 and ASIS library, AdaControl have to be run on older version of
GNAT. Also, the pretty printing unit tests is back too: same as AdaControl, old
tools suffer for problems with ASIS and GNAT. Here I replaced `gnatpp` with
Libadalang version.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week brings some fixes and new things in the console version of the
program:

* In the graphical version, there is fix for loading the icon for scripts with
  executable parameter. A bit weird that it was not crashing earlier. :)
  Probably effect of updating Tcl/Tk libraries.
* Preview for some type of text files was fixed too. Mostly the ones which can
  be executed.
* Fixed crash in console version when showing files with very long names.
* Started work on About menu in console version. For now only showing the
  program documentation files is done.
* Also, fixed showing that documentation files in the graphical version of the
  program.
* Work on the about the program dialog in the console version started too.
* Same as in other projects: updated AdaControl GitHub workflow to be sure that
  it will be using exactly GNAT 9.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl.

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Unchanged from the last week: as usual, work on fixing the problems reported by
AdaControl slowly moves forward. This week work was mostly related to the
continuing work on canonical links: the user documentation were updated with
information about them, also the name of variable version changed to lower case
to better match existing variables. And same as in the projects above: pretty
printing of unit tests is back here too. :)
