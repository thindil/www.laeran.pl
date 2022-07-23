-- layout: default
-- title: Weekly development report 2022-07-23
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Stable version looks stable for now. Perhaps until I will not look closer at
it. :) Again, nothing to report here.

In the development version, probably never-ending story about upgrading the
UI continues:

* Changed Close button in show crafting recipe info dialog to icon.
* Added new icons for all possible crafting actions, like crafting itself,
  studying and deconstructing.
* Added ability to set the icons via the game's theming system.
* As usual, updated modding documentation about the newest additions.
* Fixed position of close button in dialog to show information about the
  installed player's ship's module.
* After changing buttons in various dialogs to show icons instead of text, I
  was not entirely satisfied with the final result. I think they were too
  small. I was trying to enlarge them, but the result wasn't too good in my
  opinion. Thus, I tried a different thing: show icon and text together. ;)
  In my opinion, [the new version](https://imgur.com/lhzRhzR) looks better
  than [just icons](https://imgur.com/YjCFWRZ). That change triggered some
  other changes in the code, but now everything should work as expected.
* As almost always, some work with code cleanup and refactoring done either.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The whole week spent on working on the shell's plugins system. It's slowly going
to the end and be usable, but there still is some work to do.

* Updated the test plugin. Now it shows more options of the shell's plugins system.
* Added unit test for deleteOption procedure.
* As mentioned above, the work on the shell's plugins system continues. At this
  moment the code should be organized, and the API should be easy to extend. The
  plugins now can do any management things, like installing, enabling or
  removing. There is still work to do with API to simply using the plugins, but
  it should be a lot easier to do.
* Added plugins' API option to read the shell's configuration option.
* Started work on civilizing the code. Generally, adding pragmas, documentation
  and unit tests to the newly created code related to the shell's plugins
  system. During the work there were a few errors fixed too.
* Added a couple of very simple unit tests for the shell's plugins system.
* For the project organization: enabled to show all errors during debug
  compilations. It is useful when tracking effects and exceptions raised by
  subprograms. Especially when the first effect is something generic like
  `RootEffect`.
