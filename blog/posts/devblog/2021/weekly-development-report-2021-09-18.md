-- layout: blog
-- title: Weekly development report 2021-09-18
-- filename: blog/posts/devblog/2021/weekly-development-report-2021-09-18.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

This week again quiet in the stable version. It means that the last fixes for
the found bugs can be released. :) In around 24 hours since this post, a new,
more stable version of the game will be available to download.

The development version is slowly moving in its direction:

* Started and almost finished work on manipulating various lists in the game,
  like items to trade or crew members, with keyboard. As always, it took a lot
  more time than expected, but I'm slowly start liking the effect. :)
  Generally, the most time spent in the task was on finding the proper way to
  do it. After that, all things just jumped to their proper positions. I think
  in the next week finally will be something to show. :)
* Limited the amount of possible skills (standard plus skills defined in the
  game modifications) in the game to 64. For now, it should be enough, if not,
  then the limit will be raised.
* The change above also triggered some changes to the game documentation,
  mostly related to modding of the game.
* Fixed that Escape key in some cases doesn't close various dialogs but show
  the map.
* Standard, a few more problems reported by AdaControl fixed.
* Work on preparing the game code for formal verification continues. And it
  took the most time in this week. The side effect for it is that the game now
  use a bit less memory and works a bit faster. That means it should be
  possible soon to run it on lightbulbs. :P
* Again, some small work related to the project organization, mostly fixing
  helper scripts.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The beginning of the report is the same as in the previous week: the work on
package `Tk.Bind` is almost in the same place. More code was put in converting
`Key_Syms_Type` to `String`. The most keys should be now mapped, but there is
still something to do. Also, the unit test for the function was constantly
updated. The work on *sparkification* of the library is going forward. The
library can be used in SPARK code. The only package which can't be used in
SPARK (at least in its 2020 version), is `Tcl.Commands` due to heavy usage of
pointers. Now the work started on reaching the higher level of SPARK
compatibility. Currently, it is on `Tcl` package. And looks like it will
trigger a lot of changes to the code. :)

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

A bit more things are done in the project that in the last weeks:

* The ROOT and Polish translations updated with the missing translations
  strings.
* The dialog to execute file or directory with the selected command in the
  console version of the program is now fully translated.
* Also, fixed some bugs related to the executing files or directories with the
  selected command in the console version.
* Work on code cleanup, merging the graphical and console versions are slowly
  moving forward.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Copy and paste from the previous weeks (added *s* here :P): fixing the problems
reported by AdaControl continues. Work on the package `Sitemaps` slowly going
forward. Also, added some missing code documentation to package `Sitemaps`.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

And time for the almost annual update to the page. :) This time no big
revolution, only small changes. As the devblog slowly grows with almost every
week similar content, the main page of the blog got redesign. Devblog and posts
are separated plus the devblog is separated on years. That should make the look
a bit more clean.
