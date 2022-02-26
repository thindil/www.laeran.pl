-- layout: default
-- title: Weekly development report 2022-02-26
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version, nothing to report. At least, I can't find any bugs
there. Would be good if someone can confirm lack of problems. :P

In the development version, the almost never ending saga of updating UI
continues:

* Now all arrows for moving the player's ship or map around should have their
  own icons. That was the main focus of the week. This mean not only a few new
  images but also some changes in the code. There is still some work to do, so,
  I think, there will be something to show in the next week or two.
* The change above also triggered some changes to the documentation related to
  the game modifications.
* A lot of changes, invisible, I hope, for players in the game's code. They are
  related to the code cleanup and generally hunting unexpected features called
  bugs. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Well, that was a big week for the Nish. It reached it first alpha, very basic
and limited release **0.1.0**. :) After a few moments of celebrating,
everything back to normal and work continues. Some changes in this week list
are landed in the release some added after it.

* In release: added support for merging commands with `&&` and `||`. It works
  similar like in others shells. When merged with `&&` commands execute each
  after other, when merged with `||` the second command will execute only when
  the first was failure.
* In release: the documentation about merging commands was added to the
  project's documentation.
* In release: also shell help system updated with information about merging
  commands.
* In release: fixed handing long options in the user entered commands which
  don't have values
* In release: the default path to the shell's database should be now more OS
  friendly, especially Windows.
* In release: added a special argument to aliases which contains all arguments
  entered to them.
* After release: started work on better looking form for adding a new alias to
  the shell. It is almost finished, but need some polishing. Now the form
  should be more user friendly. Additionally, it now check correctness of the
  user input during adding the alias.
* After release: updated documentation of the project with information about
  requirements for aliases' names and working directories.
* After release: started work on made the code a bit less ugly. For now I'm
  trying to remove triggering exceptions by various subprograms.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This time copy and paste from the previous week. The complete week spent on fixing
the problems reported by `gnatprove`.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. I was thinking that I finishing the work on the
  graphical version of the program in the last week, but looks like there is
  still some work to do. :) And that was done in this week.
* Some project organization: started work on the project's configuration for
  checking the console version of the program with AdaControl. For now it is
  "work in progress", I hope that everything will be set in the next week.
