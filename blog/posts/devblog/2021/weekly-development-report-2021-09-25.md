-- layout: default
-- title: Weekly development report 2021-09-25
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another quiet week in the stable version. No bugs reported, plus I'm blind and
don't see anything. My guess: yet. :)

The development version in this week has even something to show:

* The work on manipulating various lists (like ship's crew members or cargo)
  are done for now.  A bit too long video is [here](https://i.imgur.com/a4lWNoi.mp4). :)
  At this moment, I'm quite happy with the final effect, thus time to go to
  another work.
* Started work on configuration option to set the maximum amount of items on
  various lists (for example, trading items). Earlier it was hard-coded to 25
  items, now it can be set in the game options from 5 to 100. Currently, only
  setting added and lists on ship info screen updated to use it.

Now time for some technobabble things:

* Standard, a few more problems reported by AdaControl fixed.
* Preparation of code for use of formal verification tool very slowly moves
  forward. I'm also changing how the whole process will be done. Instead of
  jump directly to the verification, I will split it on a few smaller steps.
  The first stage: end the preparations. :)
* Because checking with AdaControl slowly takes too much time, at this moment
  it takes around 30 minutes on GitHub actions for around 1/6 part of the
  code, I've decided to split it on a few jobs. The first checks only the
  project's coding standard, the second do more expensive checks. These
  changes also triggered some changes to the project organization. But looks
  like, for now, everything works as expected. :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The work on `Tk.Bind` was very short this week. It is still on creating
function to convert `Key_Syms_Type` to `String`. A few more keys are mapped and
the unit tests for the function are updated either. The main work in this week
was on *sparkification* of the library. As SPARK doesn't allow functions to
have side effects, it triggered changes to the most basic code in the library:
all `Tcl_Eval` functions are changed. They now returns record not only with
result of the evaluation but also with code returned by the Tcl command which
was evaluated. Also, the generic version of `Tcl_Eval` for scalar types are
replaced by the normal functions. These changes triggered a lot of changes in
the library code. Probably for now even the demo program doens't work. From the
project organization: the default mode for *gnatprove* changed to *check* for
now. It affects GitHub workflow action and the Bob commands to check the
library and the demo program.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

A lot of work was done under-the-hood this week:

* Work on code cleanup, merging the graphical and console versions are slowly
  moving forward. This took the most time in this week. But at least a few
  packages are cleaned.
* Fixed refreshing preview in console version after closing message and
  canceling creation of items.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Copy and paste from the previous weeks (added *s* here :P): fixing the problems
reported by AdaControl continues. Work on the package `Sitemaps` looks
finished, now it will go to the last package, `Sever`.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

Only small continuation of the work from the previous week. The layout of the
blog entries was updated to work with the new organization of the blog. And now
the whole project is going to sleep again. Probably for another year. :)
