-- layout: blog
-- title: Weekly development report 2021-10-23
-- filename: blog/posts/devblog/2021/weekly-development-report-2021-10-23.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This week, the biggest visible change in the
projects' organization is that I started using [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
style for the VCS commits. At least now it looks very clearly on what I'm losing
my time, instead of adding new things or fixing bugs. :) At this moment I
really like this style of commits. We will see how long I will stay with it.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another week with delivering several fixes to bugs. There are left a couple
of them, all related to the UI, but unfortunately, fixing them require
changing a lot of code. They will be soon or later fixed in the development
version of the game (work even started, as will be mentioned below). But
again, time to bring these fixes to the players. In around 24 hours since
this post, another, a bit more stable version of the game will be available
for download.

The development version, as usual, slowly moves forward:

* The same problems from the stable version solved now here too.
* Added (as suggested by one player) option to reset the game keyboard
  shortcuts in the options screen to their default values. Each button resets
  only shortcuts from the selected tab/group. We will see how it will work.
* Fixed scrolling with mouse wheel on Windows. This should finally work as
  expected everywhere. :)
* Fixed showing the list of workshops when setting study or deconstructing
  items orders when there are more than one alchemy lab installed on the
  player's ship.
* As mentioned above, started work on fixing in-game menus. Exactly, the
  problem with not working keyboard shortcuts in the main menu of the game on
  Windows. This requires a lot of changes to the code, but all the menus
  should look similar after that. At this moment, work almost finished on
  destination menu. I hope in the next week there will be something to show. :)
* Plus, as usual, a lot of work under the hood with code beautification. At
  least this should not generate any new bugs. :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Hello almost maintenace mode. :) The whole week spent on fixing various
problems reported by AdaControl and Gnatprove. Nothing new was added to the
library this week. But at least, now almost all problems reported by AdaControl
should be fixed. Also, some subprograms should have a better precondition
checks. Another good thing: the demo program now works properly with the newest
version of the library. Fortunately, this didn't require too many changes. On
the SPARK front the most time now is taking to write the safe version of
`Integer'Value` aspect. It is slowly moving forward, but still a few things to
prove or fix. Overall, the amount of Gnatprove checks to fix is still around
1000. :)

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The work on clearing the project code is finally finished. At least for now.
Thus, the focus now returned to the console version of the program. But the list
of changes is still a bit short:

* Fixed clearing preview after closing Actions menu, cancelling a few actions,
  like creating a new link or moving items.
* Finished work on merging the common code for the graphical and console
  versions of the program.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes.

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Copy and paste from the previous weeks (this time word *Almost* was removed :P):
fixing the problems reported by AdaControl continues. The list of rules was
updated once again, and again because it was reporting problems from AWS
library. At least there is small light in the tunnel that can point to the end
of the work. Or on another incoming train. :P
