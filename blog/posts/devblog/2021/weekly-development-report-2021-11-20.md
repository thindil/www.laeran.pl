-- layout: default
-- title: Weekly development report 2021-11-20
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

I'm not sure if I should be happy about that, but finally I found something to
fix in the stable version. :) It not always delete saved games files after
finishing the game. This mean, in around 24 hours after this post, the new
version will be available for download.

In the development version of the game, busy week as usual:

* The work on more informative headers for various dialogs finished for now.
  This took the most time in this week.
* Fixed the same problem with not deleting saved games files like in the
  stable version.
* The help topics list now properly scrolls to the currently selected help
  topic when launching the help window from another screen in the game.
* The most visible things in this week: added option to assign the crew
  members during [setting the crafting order](https://imgur.com/A4VILqp). This
  should reduce a bit micromanagement related to the crafting.
* Another thing related to the setting crafting order UI: small, but worth
  mentioning: the button for setting the crafting order now change it label
  based on the type of crafting order to set. For example, for deconstructing
  it will be *Deconstruct* for crafting will be *Craft*.
* In-game help updated with information about the new assign system during
  setting crafting orders.
* Also, in-game help got some fixes for various typos there.
* Fixed crash when showing the selected workshop menu when it has set crafting
  order.
* As always, code cleanup with static code analyzer. It again triggered some
  big changes to the code, not visible for players. At least, I hope not
  visible. :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

After some tries, I decided that the new approach to the conversion of
`Colors_Names` enumeration values to String isn't the best option. The colors
name in Tk are (fortunately) regular, thus they can be easily converted from
and to Ada Strings. Thus, I used the same approach as in `Tk.Bind` package. This
is now done, same as the proper unit tests for subprograms which convert
values. The various `Color_Type` types used by packages are merged into one
type and added subprograms to convert the type to Ada String also. And unit
tests for them. :) After that, all fields in various records related to the
colors changed from `Tcl_String` type to `Color_Type`. This task is
finished for now too. From the other things: the code documentation for a few
subprograms updated either.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The most work this week was in the console version of the program:

* The main menu of the program in the console version is now fully translated
  and translatable.
* This of course, triggered an update of translations of the program.
* Fixed refreshing the preview window after closing the bookmarks' menu in the
  console version.
* Fixed typo in the error message when the user is trying to enter non-existing
  directory from *Enter your destination* option in bookmarks menu in the
  console version.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

The work on the pages related to the [Ada Linux Package Repository](https://www.laeran.pl/linuxada/index.html)
slowly moves forward. The main page has now more information about the
available Linux distributions and CPU architectures also added documentation
about packages requirements and tutorial how to create Debian package for a
simple program.

From under-the-hood, the default template for pages got option to set custom
link for *Back* button. This should reduce amount of needed templates in the
future (when I finish basic work on Ada Linux Package Repository).

### [Ada Linux Package Repository](https://www.laeran.pl/linuxada/index.html)

*Various Linux distributions repository with programs and libraries related to
Ada programming language*

The work on the repository documentation continues. But this was mentioned in
the section above. :) From the packages: added new repository for *Raspbian*
distribution. Also, Debian and Ubuntu repositories now also available for
*arm64* architecture. This triggered fixes for packages `python3-e3-core` and
`extrafont` to made them more various CPU architectures friendly. At this
moment there is "small" problem with Debian Testing repository: due to some
problems, packages `libxmlada` and `gprbuild` are removed from the official
Debian repository. I hope it is temporary, as far I see [the work on fix](https://tracker.debian.org/pkg/gprbuild)
is under the way. So, here also everything **should** back to normal too.
