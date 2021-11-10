-- layout: blog
-- title: Weekly development report 2021-10-02
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This time the list is almost standard.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Referring to my previous week post, yes, I'm blind. :) Some brave soul started
playing the Drones faction and found a whole horde of problems. Now I'm slowly
fixing them, still several are waiting. At least I will have something to
report in the next week, too. :)

The development version is going slowly forward, this week spent mostly on the
under-the-hood work, not too much visible changes:

* Bugs found in the stable version fixed here too.
* A few newly introduced, development exclusive bugs fixed either.
* Finished updating various lists in the game to use the setting for amount of
  items to show on one page.
* Standard, removed some problems reported by static analyzing tool. That
  again triggered a couple of big changes to the code.
* Some code cleanups, refactoring, etc.

And as standard ritual: because since the last development release has passed
four weeks, it is time for another one. Around 24 hours after this post, a new
version will be available for download.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The whole week spent on playing with *gnatprove* and fixing all the problems
which it reported. It triggered a lot of breaking changes to the library API.
Mostly related to the `Tcl_Eval` and `Tcl_Get_Result` bindings. At this moment
the work is on removing `Tcl_Exception` from the library. All these things
caused that the demo program completely not working for now. Unit tests for the
library also require updates. A lot of fun. :)

From the smaller things, I've replaced `Big_Integer` with `Long_Long_Integer`
in a few contracts. This mean that flag `-gnatX` is again not needed for the
library compilation. Plus added simple wrapper functions for converting Ada
Strings to C characters array. All these changes greatly reduced warnings from
*gnatprove* about missing `Global` aspects. Not related to the *sparkification*
process: a few bindings were fixed too.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

A lot of work was done under-the-hood this week thus the list is very short
today:

* Again, the main effort this week was on code cleanup, merging the graphical
  and console versions code.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Copy and paste from the previous weeks (even not added s here this time :P):
fixing the problems reported by AdaControl continues. Work on the package
`Server` is slowly going to the end. We will see if it will be finished in the
next week.
