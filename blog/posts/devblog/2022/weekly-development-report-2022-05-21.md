-- layout: default
-- title: Weekly development report 2022-05-21
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

If you ask long enough, someone will finally help you. :) This could be a
summary of this week in the stable version of the game. One player pointed me
to two problems related to the game, and I also found a few more to fix. Well,
at least the game should have a couple issues less. :) Which mean, in around
24 hours since this post, the new, more stable version of the game will be
available for download.

In the development version, again, most of the week spent on playing with the
game code, instead of adding new things:

* Fixing the same bugs which found in the stable version of the game.
* The development version is mature enough to have the own, unique bugs. A
  couple of them are fixed now either.
* Added limit for maximum amount of ships' modules prototypes which can be
  declared in the game. The limit is now 1024 which should be more than
  enough. :)
* Similar limit added for maximum amount of items prototypes which can be
  declared in the game. It is also high, thus shouldn't be a problem. The
  both changes are more related to the modding of the game, thus a normal
  player shouldn't even notice them. But can notice a smaller size of the
  game and, at least it looks like, a less memory usage.
* As mentioned above, same as in the previous week, a lot of changes to the
  code, invisible for the players.
* Plus, the work on better looking code of the game is slowly moving forward.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The work under-the-hood continues. The whole week spent on playing with the
code of the shell.

* Cleared the code of the unit tests. All the common code should be now in the
  separated modules.
* Finished work on the first version of LimitedString type. It is very similar
  to the normal `string` type, but it has also maximum capacity. Which means it
  is something between C array of characters and Nim `string`. Personally I
  prefer to use that kind of string especially when have to deal with the user
  input. It can prevent some issues, especially related to the too long
  strings. Now the work on the type is focused on adding the code documentation
  and probably later some small changes.
* I also started using this *LimitedString* in the shell code. This triggered a
  lot of changes in the code. At least the shell compiles again. :)
* Started work on updating the unit tests to use *LimitedString* too. Here also
  will be some work to do, but I hope to finish it in the next week.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week is continuation of the work from the previous one:

* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl.
* Added keyboard shortcut to close the program in the console version.
* Changed the default keyboard shortcut for closing the program. As the console
  version has some problems with handling Ctrl-q I changed it to Alt-q. Of
  course, it is possible to change it back in the program options.
* Added showing the bookmarks' menu with the keyboard shortcut in the console
  version of the program.
* Added showing the search form with keyboard shortcut in the console version.
* Added deleting files and directories with keyboard shortcut in the console
  version.
* For similar reason like with default keyboard shortcut for closing the
  program, also default shortcut for deleting files and directories changed to
  Alt-r.
* The program documentation updated again with the information about the last
  changes visible to the users.
