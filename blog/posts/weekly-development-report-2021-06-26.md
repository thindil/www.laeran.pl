-- layout: default
-- title: Weekly development report 2021-06-26
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version, looks like all the problems which I know are fixed.
Probably a whole other world of bugs is hidden somewhere. :) Anyway, as the
game is more stable, time for the next release. In around 24 hours since this
post, it will be available everywhere where the game is. And probably one day
later I will find something again. :)

The development version is going in it own pace. And generally in forward:

* Work on redesign of bases schools screen is finished for now. There are no
  visible changes since the last week, thus the previous screenshot is still
  valid.
* In-game help got update with information about the new school.
* The screen with the saved games to load was [redesigned](https://imgur.com/bYQxJpG)
  either. I'm still not sure do I should add something there or leave in the
  current state. After removing unneeded buttons, the whole screen looks a bit
  empty now.
* One of the paper-cuts things: now during buying or selling items on trade
  screen, the game shows not only max amount to buy or sell but also
  [overall cost or gain](https://imgur.com/sYI0wrP) of the buying or selling.
* As always, technobabble: some problems reported by the static analysis tool
  were fixed. Also, some other work under-the-hood was done too. But one thing
  here could be interesting for players also. I started playing with the
  compiler optimization flags, especially with *linking time optimization*.
  While the Linux version of the game got minimal change in size, then the
  Windows version was reduced from 24 MB to 7 MB. I must say it is a pretty
  impressive change. o.o Now, the Windows version is around 90% smaller than
  the previous, based on GTK. :D In the next week I will be playing with the
  other setting too. We will see if it will have any impact on the game also.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The bindings for the Tk **image bitmap** commands are added to the library.
Same as unit tests for them and the full code documentation (I hope, useful).
Also, the code documentation for package `Tk.Image.Photo` is finished. Added
binding for the Tcl C API `Tcl_EvalFile` function to the `Tcl` package. And as
usual, unit test for it. And started the main work of this week: redesign the
demo program. The previous version was just a window with one button, the new
will be a simple calculator. At this moment work just started, but as a side
effect of it, there will be some changes in the library API too. Mostly related
to simplify some tasks. From the other work: I reviewed the code a bit and
added in a few places default values to some types and arrays. This should make
the library a bit more stable. And started fixing some missing code
documentation too.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week was almost complete copy of the previous week:

* Continue work on setting the program in console version. It is now possible
  to set all the program's keyboard shortcuts in the console too. It was
  required some more work on how the keys are handled in the console version,
  but now everything should work properly.
* Started work on setting the user defined commands in console. At this moment
  it can only show existing commands, no ability to add a new or edit any
  existing.
* Bug with showing long directories names during confirmation of their deletion
  in the console version was fixed too.
* Another bug, this time in the graphical version of the program was fixed: it
  is now possible again to add the user defined commands to the program.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl. Some things probably never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

AdaControl still reports problems in the `Config` package. Thus, the whole week
was spent here on fixing them. Also, the code documentation was reorganized to
this same manner as it is done in my other projects. And I've started some fun
with the compiler flags. For now, only setting rpath on Linux was added to the
project *yass.gpr* file and the build script was updated to the new version of
the project's configuration.

### [Docker Ada](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

Just small change here. I finally found a solution to not working linking time
optimization (especially on MinGW). If someone has that same problem:
when GCC fails to link the executable with `-flto` set on file *lto-wrapper*
then you have to install *make* package. Quite obvious. Yes, that's sarcasm.
Anyway, all the *Adabuild* images were updated by adding *make* package. The
project documentation was updated either. Again, this project is going to sleep
for now.
