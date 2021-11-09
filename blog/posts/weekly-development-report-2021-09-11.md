-- layout: blog
-- title: Weekly development report 2021-09-11
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

If you dig deep enough, you will find something to fix. :) In the stable
version, I found that space key sometimes react weird. It is now fixed.
Because it doesn't cause any crashes, I will wait with the next release to the
next week and check if I can find even more problems. Or if someone can point
me to them. Except not working on with older version of GNU libc on Linux.
That one problem need a lot more work. At this moment, the only way to fix it,
is to use the Windows version of the game, eh. :(

The development version work going in the normal, slow speed:

* Finally, finished work on sorting various lists in the game. The last thing
  were the lists in the game statistics screen. At least one task done. :)
* Added some limits for modifying the game. I guess that no one needs, that
  attribute can have a name or a description 2 billion characters long. I
  reduced possible lengths to some more reasonable values. Also, the amount of
  tools qualities settings for the skills is now limited to 16 positions max.
  The reason of this change is same as above. If these limits will be too
  strong, I will raise them later.
* The change above also triggered changes to the game documentation.
* As usual, a few more problems reported by the AdaControl tool fixed too.
* General work on some redesign of the code of the game continues. That
  sometimes triggers a lot of changes in the code, but looks like everything
  works as expected.
* Some small work related to the project organization done either.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Same as in the previous week: work on package `Tk.Bind` in on the way. Now it
is on the creating the function to convert Key_Syms_Type to string. It is
slowly moving forward, with constant updating the proper unit tests. Thus,
looks like everything works as expected. The code of the demo program is now
ready to be checked with SPARK. All things which cannot be proved are moved to
the separated package. The work on *sparkification* of the project continues.
This time it triggered to add `Window_Attribute_Type` in `Tk.Wm` package to
use with `Get_Attribute` functions. Of course, that change was triggered also
changes in unit tests. Another thing related to SPARK: as I'm slowly fixing
the problem reported by it, I have to use package `Ada.Numerics.Big_Numbers.Big_Integers`
for some subprogram's contracts. Unfortunately, GNAT consider that package as
an extension to the Ada and not a part of itself. Thus, a new compilation flag
is needed for library: `-gnatX`. And at the end of the week, there were done a
few small things related to the project organization.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

As the work on Tashy finished, the work on the Hunter slowly back to its slow
pace. But this week changes are short as in the previous:

* Fixed package `Modules` so it doesn't need `Tk` library anymore. This
  triggered some changes in the whole code either. But at least, now, the
  console version of the program can be build fully headless. :)
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Copy and paste from the previous weeks (added *s* here :P): fixing the problems
reported by AdaControl continues. Work on the package `Sitemaps` slowly going
forward. And as in the others projects, I started using dedicated AdaControl
Docker image for it.

### [TASHY](https://www.laeran.pl/repositories/tashy)

*Ada binding to Tcl/Tk, based on TASH*

The setup script updated to fix a few small problems inside. Also, the
project's changelog file updated with information about the last changes to the
library. And this means that the new version is available for download. :) The
work here is done again for some time, so the project is going to sleep again.

### [DockerAda](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

Last time the project back to the list like boomerang. :) As the new version of
Tashy was released, the images *Adabuild* and *Adabuildwin64* updated to use
the new version of it. Also, there is a new image available now: AdaControl got
its own image, as it need the newest version of Tashy too. And the work here is
also done.
