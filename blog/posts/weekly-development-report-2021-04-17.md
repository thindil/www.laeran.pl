-- layout: default
-- title: Weekly development report 2021-04-17
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The final week before the next big release ended. Everything is finished, at
least for this version. Some last minute preparations, mostly related to the
advertising of the game, will be done tomorrow. This week brings a short list
of changes:

* Finished work on redesign of the crew members' [inventory screen](https://imgur.com/jatvADP).
  That the last visible change for the current version.
* A lot of bugs were fixed this week. Especially at the end of the week (as
  usual). And I have feelings that many lingers somewhere in the shadows,
  waiting for the release day to appear.
* Some small tweaks for the UI were done too.
* And as usual, under the hood, some code cleanup and refactoring. Especially,
  the code related to the UI.

And as mentioned at the start, in around 24 hours since this post a new, shiny,
big "stable" release will be available for download.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The whole week was spent on adding bindings for various Tk **wm** commands to the
`Tk.Wm` package. Also, some missing unit tests for them were added too. The
review of missing code documenation contiues either. Default value for
`Focus_Model` were fixed too.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Again, a bit "lazy" week in the development, mostly the maintenance work:

* Standard, copy+pasted from the last week: a lot of work with fixing problems
  reported by the AdaControl. This was almost all what was done this week in
  the project. This caused a lot of changes in the code (mostly related to the
  configuration variables names). Literaly copy+pasted. :) The only change is
  that the program configuration is probably fully updated now.
* Fixed crash on showing files and directories information in console version
* Started work on setting the default program for the selected files and
  directories in the console mode. At this moment it only show the list of
  programs, it isn't possible yet to set it.

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Another week spent on the project reorganization. The unit tests of the
project were updated: no more empty tests. Added GitHub workflow to
automatically build the tests. The last thing done with the tests were added
option to pretty print them, so they will looks similiar to the rest of the
code. Also, added GitHub workflow for automatically run AdaControl check. A few
new Bob commands related to the AdaControl checks were added too.

### [Docker Ada](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

Here only one change: fixed Ada-Build image so AdaControl will not crash when
trying to check projects which use AWS library. And of course, the image was
regenerated and updated to the new version.
