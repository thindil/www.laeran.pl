-- layout: default
-- title: Weekly development report 2022-01-01
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This is the first post not only in this year but
also from the new home. I've changed my development OS from Linux to FreeBSD.
For now it looks like everything works as expected, but here is still some work
to do, especially related to the organization of the work. Generally I'm very
happy with that change, many things started work a lot better and ZFS as
filesystem is awesome. :) Now I only need to test DTrace, the second main
reason for which I switched operating system.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Of course, Happy New Year, everyone. :) Let's hope, as usual, that this one
will be better than the previous. All the best for everyone.

And now back to routine. Welcome to the first of the series of very boring
reports before the new stable version. The most of the time in the week spent
on clearing and styling the game code. There is a small chance that it not
break anything. :) This week also brings some visible changes:

* Added ability to set keyboard shortcuts related to resizing various sections
  of information in the game. Like the ship information screen or the
  knowledge screen.
* Added tooltips to the options' sections buttons, it should be now more clear
  for what each section is for.
* Technobabble: due to a lot of changes in the code, the unit tests of the
  game updated either. I temporarily raised the amount of errors reported by
  AdaControl, thus the work should now go a bit faster than earlier.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Almost copy and paste from the previous week, removed some things, so the
report is even shorter than usual. The whole week spent on fixing
the problems reported by gnatprove. The work is slowly moving forward
here.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The work here was almost identical like in the previous week:

* Back to clearing the code of the console version of the program. This time
  I'm focused on various dialogs there. Many parts of their code is common,
  especially related to creating and deleting dialogs. These parts are now
  moved to the separated procedures. And the work started on reviewing the code
  to replace the old code with the new.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

A quite busy week here. The shell is still in a very basic state, but its code is
slowly looking good. At least for me :) Some details about the work:
* Fixed using arrows' keys when the shell's history is empty
* Now only visible characters are added to the user input
* Fixed conversion of the user's home directory path in the shell's prompt
* All code should be now GC safe. There are no global variables and everything
  is nicely put in the proper subprograms.
* Removed the code related to the handling Control-C event. Due to how the
  user's input is handling now, it was unneeded anymore.
* Added command line parameter for the shell to show version and legal
  information about the shell.
