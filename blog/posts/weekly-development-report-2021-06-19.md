-- layout: default
-- title: Weekly development report 2021-06-19
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This week work was back to the normal schedule.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version, the best describe Woody Allen quote: *If you want to make
God laugh, tell him about your plans.* I was hoping that I have been able to
do a new release this Sunday, but literally today I found a few problems
related to the keyboard shortcuts. Thus, it has to wait a bit longer, before
I fix everything.

The development version goes forward almost as usual:

* I've started redesign of the school screen. With the old, the main problem
  was that it was needing a separated mouse auto-clicker for proper work. :)
  The reason of it is that every training session gives random amount of
  experience, and it cost depends on the trained skill level plus trading
  skill of the assigned trader. Thus, it can change after each training
  session. The most of this week I was spent to trying to find a good solution
  to this problem. And [here](https://imgur.com/YcLlBaP) is the current
  result. The player can now set or the amount of trainings or the amount of
  money which want to spend on training. It still needs some work, thus
  probably in the next week redesign will be finished.
* Added missing headers to a few dialogs.
* The most of the under the hood work was finished. Now it will be focused
  only on fixing the problems reported by static analysis tool, AdaControl.
  But it should take a less time in everyday schedule.
* And as usual, a few other bugs were squashed and a few new added.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The work on the bindings for Tk **image photo** is finished. All should be on
their right place. Also, unit tests for them are done too. The documentation
for the package `Tk.Image.Photo` is also finished. The whole new code was
checked with AdaControl too and all looks ok. At least with currently enabled
rules. :) There were some small changes to previously created bindings for
**image photo** for keep everything in the same manner. Plus some small changes
to GitHub workflow for the project testing suite.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The work on ability to set the program various configuration in the console
version slowly moving forward:

* All the program's main options can be set also in the console version. At
  least these options which have sense in console. So, there no option to set
  to use monospace font in text preview or size of icons. But all the others
  are works as expected.
* Started work on setting keyboard shortcuts for the program. This work was
  just started, so for now it is only possible to show them to the user and
  travel around them.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl. Some things probably never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

And we very slowly move forward here with fixing the problems reported by
AdaControl. But still in 1/3 of the whole checks, this week in `Config` package
body. Second thing done this week is started work on updating the code
documentation to use the same structure like in the other projects.
