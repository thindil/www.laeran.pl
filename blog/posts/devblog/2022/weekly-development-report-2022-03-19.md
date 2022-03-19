-- layout: default
-- title: Weekly development report 2022-03-19
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

As always, the worst bugs are hidden in plain sigh. Fortunately, one player
pointed me there. As it was really game stopper, it got a fast fix plus
another, more stable version of the game. And let's hope that was the last
from the big bugs there. :)

In the development version week as usual:

* Almost finished work on UI icons. I think [the ship info screen](https://imgur.com/xkAKXzW)
  looks now a bit better. I'm still not convicted to the icons used to maximize
  or minimize information's sections. Maybe in the future I will change them.
* As usual, the modding guide and general documentation of the game updated with
  information about the new icons and how to customize them.
* Some bigger changes in the code done either. This time it caused one of my
  favorite types of bugs: the game started crashing in one place when the
  problem was in completely different. It took me some time to find it and fix,
  but now everything should work as expected, unless there is something more
  hiding in the shadows. :)

And four week tradition is coming: a new development version will be available
to download in around 24 hours after this post, so everyone will be able to
join the fun in finding a new “features”. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The work on making the shell and its code look better, going on.

* Again, a few more subprograms don't propagate exception around, they all are
  nicely handled now with showing the proper error messages to the user. This
  also triggered some updates to the whole shell's code, especially for
  subprogram's pragmas.
* Showing detailed information about the selected alias should now look a bit
  better.
* List of available shell's configuration's options updated either, to be in
  style with all other shell's information.
* Generally, the output header got some margins around, thus it now looks more
  centered.
* Added saving stack trace information when exception occurs. It works only in
  debug build of the shell as only in this mode stack traces are generated. The
  new debug log file is created by default in user cache directory. It is
  usually /home/user/.cache/nish on Unix.
* Finished work on adding types to the all variables in the shell's code.
* Started work on adding statement `using` to the shell's code modules. This
  work same as adding types should finish soon.
* Started work on better code documentation comments.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This time copy and paste from the previous week. The complete week spent on fixing
the problems reported by `gnatprove`.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. Still at the graphical version of the program. :)
* Revert changes to the AdaControl rules setting. Looks like they don't work
  properly.
* Fixed showing the main menu in Trash in console version of the program.
* All previous options available in Trash works again in the console version of
  the program.
