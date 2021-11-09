-- layout: blog
-- title: Weekly development report 2021-08-28
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This week has more entries, caused by general
"sparkification" of my code. :)

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

They said that the best place to hide is plain sight. And I see some of my
bugs know this rule. :) Just caught two of them, related to entering a wrong
value in numeric fields, like amount items to buy or sell, etc. This mean
that in around 24 hours since this post, a new, a bit more stable version of
the game will be available to download.

The development version going forward in its own pace:

* The list of available missions in bases now can be sorted.
* Started work on sorting abilities for the list of available items to loot
  from empty bases.
* Also fixed the same bugs which were found in the stable version. Plus,
  sorting of accepted missions by time and reward should now work properly
  too.
* Technical babble: The most work in this week was related to prepare the code
  for formal verification tool. This triggered either work in the GUI library
  used by the game, fortunately it is my library, so I can quite fast implement
  needed changes. :) But for now, I didn't add any new formal checks. Instead,
  I started working to redesign some core code of the game, so it will work
  with the formal verification tool. During the work, I noticed that the
  changes caused some memory leaks. It took some time, but I think the most of
  them are now fixed. There is  still “a few” things to do, they should be
  fixed in the next week. Also, some organization work related to the formal
  verification of the game made too. And of course, the fun with fixing
  problems reported by AdaControl continues. :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

As promised in the last week. The whole this week was spent on adding various
keysyms supported by the Tk library to `Tk.Bind` package. And here is still
some work to do with it. But the main work in this week was focused on making
the library more SPARK friendly. At this moment, it means adding default values
in many records and fixing precondition contracts for various subprograms. A
bit strange that GNAT doesn't detect the problems with preconditions. Also,
unfortunately, the whole library will not be fully formally verified, mostly
due to way how adding new Tcl commands is made. But the most specification
should allow use it in SPARK code. Also, I will try to formally verify as much
as possible of the code. For now as a main testing field is used the library
demo program. The goal is that it should be almost fully SPARK ready. At this
moment I'm trying different approach to the adding new Tcl commands in
`Tcl.Commands` package. We will see if it works or not. Also, added some Bob
commands to run verification a bit easier in console. And another GitHub
workflow with checking the library with *gnatprove*. :)

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Work on clearing the program code and updating the console version of the
program slowly moves forward, but unfortunately, due to work on Tashy, it
almost stopped at the end of the week:

* Work on merging the same code from graphical and console version of dialog
  with information about the program continues. Now the console version should
  be finished either.
* Small update to messages in graphical version code to work with the new
  version (not released yet) of Tashy.
* Standard, almost copy+pasted from the last weeks: some work with fixing
  problems reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Copy and paste from the previous week: fixing the problems reported by
AdaControl continues. It is still at the `Pages` package. That going very
slowly forward. But this time also the project documentation got some updates.

### [DockerAda](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

The adabuild image was fixed with missing GPR_PROJECT_PATH environment
variable. Also, added showing the progress of download of SPARK. And updated
the project documentation with information about the contents of the adabuild
image.

### [TASHY](https://www.laeran.pl/repositories/tashy)

*Ada binding to Tcl/Tk, based on TASH*

After almost one year of break, this project is back to life again. :) Main
reason is try to formally verify Steam Sky. This requires to make Tashy a more
SPARK-friendly. The whole library will be never formally verified, probably only
**Tk** bindings' specification will be checked for SPARK correctness. But even
this should help a little. At this moment only few packages are 100% sure that
work with a SPARK code, still more work to do. Also added function
`Arguments_To_Array` which allows convert C arguments of Tcl commands to Ada
array of Unbounded_Strings.
But the most important information is that this version **will contain possibly
breaking change**: the type `Tcl_Interpreter` was changed from a pointer to
`System.Address` so it can now work with a SPARK code.
