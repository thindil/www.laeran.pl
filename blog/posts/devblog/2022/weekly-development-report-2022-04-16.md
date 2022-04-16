-- layout: default
-- title: Weekly development report 2022-04-16
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. Foremost, happy holidays, everyone. And after a
short celebration, back to the topic. :)

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version, the week without any bug report. Weird, probably the
ticket's system stopped working. :)  Thus, there is nothing to report.

In the development version, another week designed for spring-cleaning of code:

* Added limit for maximum length of names of the modules' prototypes. It is
  now set to 64 characters, which should be enough in most cases. If not, then
  we will raise it. ;) That, as usual, triggered a lot of changes in the code
  and the game's documentation related to modding it. Shouldn't add too many
  bugs.
* Added limit for maximum length of crafting recipes' indexes. Same as above,
  it is set to 64 characters. And also, as above, a lot of changes to the code
  and some to the game's documentation.
* Code cleanup task is slowly moving forward either.

As another four weeks passed since the last development release, in around 24
hours after this post a new development version will be available for download.
So, everyone will be welcome to join hunt bu… easter eggs in the code. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Another week full of code cleanup, refactoring and adding unit tests to the
code.

* Finished work on better code documentation. It should now look the same for
  all subprograms and be more informative than the previous version. I still
  can't be convinced to runnable examples. Maybe in the future I will try them.
* Work on adding new unit tests to the code continues as in the previous week.
* Same with work on adding own types to the shell. It usually triggers a lot of
  changes to the code, thus work here is quite slow.
* Some other refactor things done too, mostly related to better check for
  variables values, etc.
* Started work on using everywhere named parameters in subprograms' calls. This
  will take some time but should make the code more consistent.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. This time something big changed: the graphical
  version is done, now the work started on the console.
* Updated `check.tcl` script, so it doesn't check for AdaCurses during checking
  the console version of the program. Continuation of fix from the previous
  week.
* Fixed showing path buttons after start the program in the graphical version.
* Fixed showing path buttons for destination after starting copying or moving
  files or directories in the graphical version.
* Fixed not working path buttons after finishing copying or moving files or
  directories in the graphical version.
* Of course, the program documentation updated with information about these
  changes too. :)
