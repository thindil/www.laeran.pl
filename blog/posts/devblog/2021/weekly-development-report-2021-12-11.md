-- layout: default
-- title: Weekly development report 2021-12-11
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. If I'm good count, it is around one year since I
switch from Git to Fossil as my main SCM. I have to write that I'm still very
happy from this change. Fossil is much lighter and faster than Git, also for
me, it is a much easier to manage smaller projects with it. That was definitely
a good change. :) The only downside is that Fossil is a lot less popular than
Git, thus many tools doesn't support it.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version, again, nothing to report. The next week will be the last
when something can be changed, because soon the development version of the
game will enter “bug-fix only” mode.

Speaking of which, here work going as usual:

* Finished work on ability to show and sort the player's ship's crew members
  list by their skills. It now allows showing or the highest skill name of the
  crew members or the level of the selected skill. For example, for *Piloting*
  skill it can look [that](https://imgur.com/NGCTabg). It should make the crew
  management a bit simpler. :)
* The player's ship's crew list got some improvements with various tooltips
  too.
* Another visible change is a new look of the map manipulation buttons. They
  are changed now to use arrows instead of text. It should look a bit better.
  Also, they got some tooltips.
* From modding point of the game: each type of item in mobs and ships
  prototypes can have maximum 100_000 items. This should be enough for
  everything.
* Continuing above, the modding guide should be now in closer to proper
  English language. :)
* A lot of invisible changes in the code, mostly related to cleaning it and
  preparing for formal verification. Especially the last can sometimes cause
  large amount of changes.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Finished for now the work related to changing various variables types from
`Tcl_String` to `Variable_Name` of `Unbounded_Variable_Name` types. Also, added
a new type `Max_Length_Type` for them, so now it should be easier to change it.
Then the whole week work was on fixing various problems reported by *gnatprove*
tool. Some preconditions updated and a lot of checks added to the code, mostly
in the `Tk.Widget` package. And amount of proofs to fix only raising not going
down. :) Well, this will take a lot of time, to fix them all. Also, the unit
tests updated to the new version of various subprograms.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The most work this week was again in the console version of the program:

* Added translations to the preview window in the console version of the
  program.
* Fixed setting files and directories permissions in the console version.
* Added translations to various messages in the console version.
* Started work on adding translations to the options interface in the console
  version.
* All this changes caused also updates to the program's translations.
* Some code cleanup and refactors to made it simpler.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

Only invisible changes this week. All the blog posts now use *default* template
for the pages. This should make maintenance of the site a bit simpler. As the
work here is finished, the project back to it sleep state. Probably again for
the whole year.
