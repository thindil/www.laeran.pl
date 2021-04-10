-- layout: blog
-- title: Weekly development report 2021-04-10
-- filename: blog/posts/weekly-development-report-2021-04-10.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. As the list of changed projects back to the standard
size (still a bit too big for me), this week report will a bit shorter.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another week in "All Quiet on the Western Front" style. Work slowly continues
towards a new major release, just one more week to go. This week changes are:

* Lists of player's ship crew and modules got pagination option. The work on
  the ship info screen is done. At least for now. :)
* List of available recruits in bases and items to loot in abandoned bases
  also got pagination. Now I hope at least that work is done completely.
* Some small tweaks to UI, like made some elements wider, clearing search
  entries in shipyard or list of known bases, added info about free player's
  ship cargo space to the list, etc.
* Code cleanup, refactoring, etc. Also, constant fun with fixing problems
  reported by static code analysis.
* Another few bugs were caught. Probably still a few hordes of them waiting
  to be discovered.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Code refactoring finished, at least for now. All functions which return more
than one value now return them as records not arrays. This should make a code a
bit more readable. `Tk.TtkButton.Invoke` functions were replaced by generic
functions for better flexibility. Work on bindings for Tk commands **wm** in
`Tk.Wm` package continues. Still most of them are empty, but finally I've
started adding the code to them. Also, a few new tests units were added. Plus
some problems reported by AdaControl were fixed. And the code documentation
were updated too (mostly with missing *HISTORY* element).

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Almost as usual, very small amount of work done here, mostly the maintenance
work:

* Standard, copy+pasted from the last week: a lot of work with fixing problems
  reported by the AdaControl. This was almost all what was done this week in
  the project. This caused a lot of changes in the code (mostly related to the
  configuration variables names).
* Fixed clearing preview on canceling moving or copying in console version
* Fixed unneeded clearing of selected items list in console version
* Finished work on setting permissions for directories and files in console
  version
* Fixed crash in console version when no files selected for deleting
* Added info about associated application to the directories information

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Generally, this week was spent on the project reorganization. Added more the
project documentation (like coding standard, etc.) to the [Fossil](https://www.laeran.pl/repositories/yass),
added option to build the project on Windows systems. This one at this moment tested
only via Docker image, but should work natively too. Also, the project
documentation were updated too. In code only version number was raised this
time.
