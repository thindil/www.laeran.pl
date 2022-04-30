-- layout: default
-- title: Weekly development report 2022-04-30
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Still nothing to report in the stable version. But I have some things to check
there. I also checked one old report
[about problems with lagging keys on Windows](https://github.com/thindil/steamsky/issues/90),
and it looks good for me. If someone could check it too, and inform me about
the result, it would be very nice. :)

In the development version I hoped to add something new to the game, but
again, the spring cleanup take almost the whole time in the week:

* Some breaking changes: I changed type of index of ships' prototypes list to
  numerical values only. I didn't use any other type of ships' index anywhere,
  and it is a bit faster, especially with many prototypes in the game. This
  triggered many changes to the game's code. Let's hope that not too many new
  bugs, either. :)
* Added limits for maximum owners and size for ships' modules. Both are limited
  to 10, probably bigger amounts not needed for now.
* The game's documentation about modding updated too.
* Added some better checks during loading the game's data files, especially
  related to the ships' modules. Now it should be more informative what is
  wrong in the files.
* As usual, the almost never-ending story about making the game's source code
  more readable is slowly going forward. This time it also triggered many
  changes in the code.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Finally, the spring cleanup finished. :) Back on track with adding some basic
features to the shell.

* As mentioned above, all subprograms now have corresponded unit tests. The
  most of them are still very basic, but at least they are here.
* Where it is possible, the code uses own types instead of generic. It should
  make the code more readable. Later I will change these types to `distinct` so
  it should be also less errorprone.
* All calls now should use named parameters. Again, this should improve
  readability of the code.
* Now when there is any user input in the shell, using up or down arrows to
  travel via shell's history, shows command which starts with the input. For
  example, after entering `al` in shell, using arrow up will fill input with
  `alias list` if that command entered earlier.
* Started work on editing the user's input with arrow keys. At this moment only
  moving with arrow keys is done and edition is in insert mode. More work to do
  here. :)
* Some small changes to the project's documentation.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl.
* Added keyboard shortcut to toggle visibility of hidden files and directories.
* Updated some code documentation in the console version of the program.
* The program documentation updated with information about the last changes.
