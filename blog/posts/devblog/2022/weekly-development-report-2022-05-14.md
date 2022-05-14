-- layout: default
-- title: Weekly development report 2022-05-14
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version, back to normal, no unexpected features found in this
week, no nothing to report. I need to go deeper. :)

In the development version, there are finally some visible changes too. But
most of them still related to the code cleanup and refactoring.

* Updated the game modding documentation with information about maximum length
  for items types names and their descriptions.
* Started work on some improvements to bases' shipyard user interface. For
  example, it now colors hulls' sizes on the modules to install list, if the
  selected hull is bigger than installed.
* Small updates to the game's help, mostly related to the first steps in the
  game. Let's hope that lack of fuel now will kill fewer people. At least
  these one who read the help. :)
* As mentioned above, many changes to the code related to its refactoring. The
  side effect is a smaller memory usage, as if it used to be high. The other
  side effect can be a whole group of new bugs, but we will see soon. :)
* The standard work on the code beautification continues as almost always.

And because the last development release was around four weeks ago, it is time
for a new one. Thus, in around 24 hours since this post, the new development
version of the game will be available to download.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The celebration week... or maybe the entire 5 minutes. :) Anyway, the new
version of the shell, 0.2 released. And the work on the project continues, but
this week, mostly on invisible things.

* Optimized a bit setting the environment variables. It now shouldn't delete or
  modify a variable if its new value is the same as the old one. This feature
  landed in 0.2 version.
* As usual, just after a release the new bug arrived. So, now reading the shell
  arguments should work as expected. Previously, their required a proper order
  to work.
* A lot of work related to the program unit tests. Mostly code refactoring like
  moving common code to separated modules and some better checks.
* Also the code of the shell got some refactoring work. All constants moved to
  their own modules and some types are stricter.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week is continuation of the work from the previous one:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl.
* Removed hard coded keyboard shortcut Alt-q for quitting from the console
  version of the program.
* The program documentation updated with information about the last changes.
* Continue work on keyboard shortcuts in the console version of the program. At
  this moment it is in a very early stage of the development.
