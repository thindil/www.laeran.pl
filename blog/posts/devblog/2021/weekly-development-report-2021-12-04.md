-- layout: default
-- title: Weekly development report 2021-12-04
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another almost quiet week in the stable version. With exception that there is
again problem with lack of compatibility of Linux version with a bit older
system libraries. Some day I should find a solution, but for now, all which I
know are very time-consuming.

The development version got some updates as usual:

* Added missing focus frame around some buttons. Now all of them should be
  marked when have keyboard focus.
* Same with various list boxes (like items types, faction selection, etc.).
  They have now a focus frame around when they are selected by keyboard.
* Fixed the game crash when canceling moving items from the selected crew
  member's inventory to the ship's cargo.
* Modding the game: prototype mobs and ships cargo now can have max 32
  different types of items. It should be enough, especially that the most of
  them have around 5-10 usually.
* Also, updated the game documentation with information about items limits.
* The main game menu button and close buttons now uses icons instead of text.
  They now should be much smaller, thus not draw attention from the more
  important parts of UI. [Here](https://imgur.com/wfQnZFs) is how it looks,
  with one more thing currently in work. Details are below. ;)
* Started work on some updates to the player's ship's crew list. Currently,
  it is a bit hard to find a crew member with a desired skill. I stated work
  on adding the option to select to show only members with the selected skills.
  For now, only UI is ready, the whole code with showing is in to do state. :)
  Effects are visible in the image in the previous point.
* Under the hood again, changed one small thing which caused an entire
  avalanche of the changes around the code. As usual, the code formatting and
  refactoring work is very slowly moving forward.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Almost the whole week spent on converting various `Tcl_String` to
`Variable_Name` or `Unbounded_Variable_Name` types. Also, removed some unneeded
preconditions checks, they are now done with the *Dynamic_Predicate* of the
types. And fixed again a few problems reported by AdaControl. All these changes
again reduced a bit amount of proofs needed, but the ration still is on the
same level. :) Another change: taking the options of the selected menu entry
should now work properly. All these changes triggered also changes in unit
tests.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The most work this week was mainly in the console version of the program:

* Fixed showing focus frame around directory view after canceling renaming
  files or directories in console version.
* Fixed showing focus frame around directory view in console version after
  canceling creating a new link.
* Added translations to rename or delete file or directory action forms
  in console version of the program.
* Added translations to the clear trash action in console version.
* Added translations to the info about the selected file or directory in
  console version
* Fixed not hiding the previous menu when showing *execute with* form in
  console version.
* Fixed not hiding the focus frame around directory view when showing execute
  with form in console version.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

Same as in the previous week, the work on the pages related to the
[Ada Linux Package Repository](https://www.laeran.pl/linuxada/index.html).
Added more pages for each supported distribution. Also, added a new tutorial
about creating an Ada library package for Debian plus separated page with some
useful tips when creating Debian packages. At this moment it contains only
information how to add patches to a package.

From under-the-hood, the page got some style updates, again related to showing
blocks of code. This time it really should look better. :)
