-- layout: default
-- title: Weekly development report 2022-07-02
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version, again quiet. Probably because I spend too much time with
the development version. Nothing to report here, but I'm curious about bug
reports from the other people. :)

The development version finally has something to show. Not too much, but
always some progress:

* The under-the-hood work on adding buttons to various in-game dialogs
  finished. Now it is time to start adding the new buttons.  A few dialogs
  updated with them. As the dialogs share a lot of common code, it is faster
  work than was adding the whole “mechanic”. For example, the item
  information's dialog in the player's ship's cargo looks now [that]
  (https://imgur.com/YjCFWRZ). I'm still thinking about the order of buttons.
  Now, the close button is in the middle. Maybe it should be as the last?
* Replaced texts on a few dialogs' buttons with icons.
* Added ability to set all the new icons via the game theming system, it
  should be easier to modify.
* Fixed traversing with Tab key in the dialog for giving items from the
  player's ship's cargo to the selected crew member.
* Fixed one interesting bug. Usually, I'm testing the development version of
  the game in the debug mode. When everything is ok, the development version
  is ready to go. Then I just check if the game starts and some basic actions.
  This time I wanted to see something in the previous development version,
  and the game suddenly crashed. The interesting thing is that the same thing
  works very well in the debug mode. After some investigation, I noticed that
  it must be a some kind problem with code optimization in the compiler.
  Fortunately, I was able to find a workaround, so at least this one thing
  should work properly now. Anyway, it took some time and was and an intriguing
  experience. :)
* Standard footer. The work on better code going forward, with the speed of
  drifting continents. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Again, some new things arrived in the shell. Still a lot of work to do, but
slowly, the program is going to be useful. :)

* Finished for now work on various settings for `history  show` command. It is
  now possible to set amount of the last commands to show on the list, their
  order and the direction of the order.
* The command `history show` now accepts also more parameters which allow
  setting temporary the same options which can be set in the shell's options.
  For example, `history show 10` will show the last 10 commands from the shell
  history with all other settings taken from the shell's configuration.
* Also, the shell's help's entry for `history show` now inform about all the
  possible parameters and options which can be set for it.
* The most time in this week spent on adding ability to redirect the output
  of the shell's aliases. The feature required some changes in the shell's
  database and to the aliases settings screens. But the most work done with
  the executing the aliases. It should work, but if the alias is an
  interactive alias, then only when output isn't redirected the interactivity
  works.
* Again, some updates to how the shell's database is created and updated are
  done. Now it is related to the aliases' data.
* As always, the program's documentation upgraded with the information about
  the new features.
* Almost standard task, some code cleanup, formatting and generally trying
  to make it better.


### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

Here only one small visible change in this week and probably month either. I
removed not maintained any more Linux Ada Repository related pages. And the
project is going to sleep again. Probably until I will not try to change the
look of the page again. :)
