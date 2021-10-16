-- layout: blog
-- title: Weekly development report 2021-10-16
-- filename: blog/posts/devblog/2021/weekly-development-report-2021-10-16.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This time the list is almost standard.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And again, the new stable version released, new bugs after couple days
emerged. I want to thank a few people who reported them. Now I need to start
to fix them. I hope, in the next week, I should have most of them fixed. At
this moment, only the in-game help updated.

In the development version, the most of the week spent on under-the-hood
things (again). But, a few small visible changes are also here:

* Search for various items no longer trigger the main menu's shortcuts.
* Also in the development version, the in-game help updated.
* Assigning crew members to a workshop now
  [shows information about crew members' skills](https://imgur.com/GCUuVdf) in
  the same way how it is made in combat: single plus after name means that crew
  member has needed skill, double plus after name means that crew member has
  the highest level of needed skill in the crew.
* The list of skills to train in the schools in sky bases got information
  [about the level of skill for each crew member](https://imgur.com/xqPfz26).
* Standard footer for the last weeks (and months): a few problems reported by
  static analysis tool fixed as usual. A lot more still probably exists. It
  again triggered a lot of changes to the code and updates to unit tests. But
  looks like for now everything works good.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The idea about raising the SPARK mode was good... now I have a whole legion of
problems to fix. :) Anyway, the whole week spent on fixing various problems in
the code reported by gnatprove and AdaControl. The work on the new bindings are
stopped for now. The generic versions of `Tcl_Get_Result` function removed and
replaced by normal functions. They are simpler to use and should be also
simpler to prove that they don't have too many bugs. At this moment,
*sparkification* of the library very slowly moving forward. Around 1600 various
checks are proved, still around 1000 are to fix. And then I will raise the
SPARK mode to **silver** level for even more fun. :P And now the project is one
year old. This mean it is longer in the development than the previous version
of TASHY.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week I decided to speed up the code cleanup and focused only on this task.
That is result why the report from the project is very short today. Literally
the whole week spent on two things:

* The main effort this week was on code cleanup, merging the graphical
  and console versions code.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes. (One change: removed
  emoticon here :P)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Almost copy and paste from the previous weeks (this time word *Almost* was
added): fixing the problems reported by AdaControl continues. The list
of rules was updated again, and again because it was reporting problems from
AWS library. Unusual thing: crash introduced during playing with the AdaControl
in `Server` package was fixed too.
