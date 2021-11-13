-- layout: blog
-- title: Weekly development report 2021-11-13
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Again, nothing to report in the stable version of the game… which mean I need
to dig deeper to find the bugs. There must be something. :)

In the development version, the work on updating the game UI continues:

* All the in-game menus now looks similar to each other and that same on Linux
  and Windows. This work took almost the whole week.
* Started work on giving some more information in the menus about which object
  currently manipulated, instead of just showing *Module actions* or *Item
  actions*. This should take a much less time than the previous work, I expect
  to finish it in the next week.
* Fixed crash when removing the player's ship's modules in bases' shipyards.
* As always, technobabble, code cleanup with AdaControl tool. In this week
  again it triggered one large change to the code. Plus a lot of small
  changes. :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The whole week work was focused on adding colors enumerations values to the
`Colors_Names` in `Tk.Colors` package. But at least, this one is finished. Now
I'm trying to do a different approach than with the keys names in `Tk.Bind`
package. I will create an array with index as `Colors_Names` and values of
`Tcl_Strings`. We will see which solution is better for converting Ada
enumeration to **Tk** names. That probably will take again some time. Also,
there were a few different colors related records in various packages. Now
they are unified and moved to `Tk.Colors` package.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The week of beautification of the console version again here:

* Fixed highlightning the program menu in console version after selecting its
  submenu.
* Fixed showing the frame around directory view when the bookmarks and selected
  menus are closed in console version.
* Fixed showing the frame around preview when selecting to show preview or info
  in console version.
* Fixed showing the main program menu in console version during copying or
  moving files or directories.
* Updated translations of the program.
* Added translations to the main menu of the program in the console version.
* Added translations to various sub menus of the main program menu in the
  console version. There is still some work to do, but should be finished in
  the next week. I hope. :)
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

The most of the week took work to update the project to the newest version
of [YASS](https://www.laeran.pl/repositories/yass). It means mostly removing
unneeded settings from various pages. But also added a page about new project
(in very early stage of organization), [Ada Linux Package Repository](https://www.laeran.pl/linuxada/index.html).
This triggered some small, but visible changes to the whole page style. But
this is noticeable here. :)

### [Ada Linux Package Repository](https://www.laeran.pl/linuxada/index.html)

*Various Linux distributions repository with programs and libraries related to
Ada programming language*

This is the new kid here. The main reason of creating it, is to bring more
conventional support for various Ada programs and libraries to Linux. Also, to
made installation of Ada programs easier on Linux, thus to promote Ada
language. :) At this moment, the repository is under organization. Many things,
especially related to its documentation will be changed or are still missing.
For now only a few packages are available in the repository, only for some
Debian and Ubuntu versions.
