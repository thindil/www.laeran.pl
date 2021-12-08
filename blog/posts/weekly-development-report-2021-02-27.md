-- layout: default
-- title: Weekly development report 2021-02-27
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

This week was passed definitely too fast :) The most of the work was spent on
various under the hood tasks, thus no screenshots this time.

* Started work on redesign various questions' dialog, so they will look and
  feel like the rest of the UI.
* Fixed some bugs related to loading the game configuration.

From the invisible part:

* As always, code cleanup and updating code documentation work slowly moving
  forward.
* Finished fixing coding style. Now it looks a little better than earlier.
* Started a new, big project. Some time ago I wrote that soon or later I will
  use military or avionic standards to prevent/finding bugs. And this time
  happened. I started using the static code analysis tool called [AdaControl](https://www.adalog.fr/en/adacontrol.html),
  created and used (not sure if still in use there) by [Eurocontrol](https://en.wikipedia.org/wiki/Eurocontrol)
  to check correctness of their Ada code :D Of course it still isn't [DO-178C standard](https://en.wikipedia.org/wiki/DO-178C)
  but the game very slowly going in that direction. At this moment AdaControl
  reports mostly (around 90%) style problems, but the rest 10% looks for me
  like potential problems in the code, or possibilities to optimize it.
  Anyway, fixing all these reports also will take some time. Steam Sky maybe
  will not be the best roguelike but definitely the one who can be used on
  airplanes hardware :D

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Fun with static code analysis continue. At this moment, the current binding to
the various Tcl commands and API's should be fixed. The work started now on Tk
binding. Also, the unit tests were updated to the new version of the binding
plus demo `helloworld` was updated too.

### [Hunter](https://www.laeran.pl/repositories/hunter)
:bd
*Graphical File Manager for Linux (written in Ada)*

Generally speaking, the maintenance week here, same as in other projects:

* Fixed copying and moving items in console version of the program
* Added treating all warnings as errors to the debug build of the program
* Same as with Steam Sky, started work on static code analysis with
  [AdaControl](https://www.adalog.fr/en/adacontrol.html)

### [Bob](https://www.laeran.pl/repositories/bob)

*Non-Intelligent console assistant (written in Ada)*

And here is almost literally copy and paste from the last week:
As the maintenance work continue here, the whole week was related to running
static code analysis and fixing all reported problems. Also, fixed the problem
with creating output files for the commands.

### [Ada Planet](https://www.laeran.pl/repositories/adaplanet)

*News from the Ada programming language world*

As other projects, this one also got some maintenance work:
* The page title for anonymous users were fixed (at least for English version)
* The list with the RSS feeds were updated too
