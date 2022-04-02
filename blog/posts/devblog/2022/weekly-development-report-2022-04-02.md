-- layout: default
-- title: Weekly development report 2022-04-02
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. As the new month started, time to do some cleanup
with the projects again. This time TASHY2 is going on a very long break.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

As expected, just after release of the new stable version, another bug
reported. This time during fixing and testing it I also found a few another.
They fixed too, thus in around 24 hours since this post another “stable”
version will be available for download. Let's see how much bugs this time
emerge. :)

In the development version, almost the whole week spent on the invisible
changes in the code:

* Fixed the same issues found in the stable version.
* The only visible change this week: the text for assigning the crew members
  to the workshops changed from “Work in [workshop name]” to “Work on
  [crafting recipe]”. This should be more clear, especially when a few
  workshops of the same type installed on the ship.
* This may be only interesting for people who modding the game: I've added the
  length limit for various syllables used in generating names for ships and
  crew members. The work not finished yet, thus there are no updates to the
  game documentation.
* As mentioned above, a lot of work inside the game's code. At this moment,
  it looks like it didn't create any new problems. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The work on making the shell and its code look better, going on. Same as in the
previous week, no new features from the users' point of view.

* And another week with changes to handling exceptions in the shell. A few more
  subprograms don't propagate exception around, they all are
  nicely handled now with showing the proper error messages to the user. This
  also triggered some updates to the whole shell's code, especially for
  subprogram's pragmas.
* Continue work on better code documentation comments.
* Continue work on adding unit tests to the project. Still most of them are
  very simple, but they should prevent some basic bugs in the future. Or
  at least they are nice skeletons for the real ones. :)
* Fixed getting the shell's commands history length when there was an error
  during reading it from the database.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. But something big changed. I probably finished
  cleaning the graphical version of the program. :) Now it is time for the last
  1/3 of the code: console version.
* Fixed showing the remove bookmark button in the graphical version of the
  program.
* Fixed showing the remove bookmark menu option in the console version. This
  one also triggered some changes in the code.
* Added option to close Selected menu in console version with Escape key.
