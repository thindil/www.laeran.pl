-- layout: default
-- title: Weekly development report 2021-11-27
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version back to its natural state. No bugs reported or found there.
Something wait to discover. :)

The development version of the game going forward in its normal speed. In this
week, mostly by fixing various small bugs, but it also brings a few large
changes:

* Tab traversal in the set crafting order menu should now work properly.
* Closing the set crafting order menu with Escape key also should now work.
* The same with closing the detailed info about the selected crafting recipe.
* Small updated to the setting crafting order button: it now shows what kind
  of crafting order will be set, instead of just “Craft”.
* Probably the first change which break some compatibility with the previous
  versions of the game. The configuration file for keyboard shortcuts changed
  its format on the same as the normal configuration file uses. Unfortunately,
  it will reset all custom shortcuts. That the only problem with it, the
  advantage is that now the file is more flexible and stable. It is also
  easier to add or remove keyboard shortcuts from the game.
* Fixed resetting keyboard shortcuts for the player's ship's movement actions.
* The default keyboard shortcuts for setting the player's ship's speed fixed,
  too.
* Modifying the game: the maximum length of the items' index name set to 64
  characters. Should be enough for many items. :)
* Under the hood, back to preparations of the game for formal verifications.
  Again, changed one small thing which caused a whole avalanche of the changes
  around the code. As usual, the code formatting work is very slowly moving
  forward.

Because since the last development release was almost four weeks, it is time
for another. Around 24 hours after this post, a new development version of the
game will be available for download.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The work on updating the code documentation for various `Options_To_String`
functions is finished for now. All should have some simple examples how to use
them. A few others subprograms got fixed their documentation either. A few new
problems reported by AdaControl tool fixed. The biggest changes this week are
added two new types, `Variable_Name` and `Unbounded_Variable_Name` (let's
follow Ada loooong names convention :)). They are used to setting names for various
Tcl or Tk variables, like for example `Tk_Image` identifiers. I've started
conversion of various options' fields for **Tk** widgets to these new types. It's
slowly moving forward, especially because the change also require updates to
the unit tests for changed **Tk** widgets. And the percentage of proved
gnatprove tests are still on this same level. Just the amount of proofs is
raising. :)

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The most work this week was mainly in the console version of the program:

* Fixed refreshing the currently selected directory or file preview after
  closing the search dialog.
* Added translations for the search dialog in the console version of the
  program.
* Added translations for creating new files, directories or links in the
  console version.
* Fixed the information text when creating a new link in the console version.
* Updated both, root and Polish translations files.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

Same as in the previous week, the work on the pages related to the
[Ada Linux Package Repository](https://www.laeran.pl/linuxada/index.html). The
tutorial for creating a simple Debian package updated with some clarifications
and fixes for typos. The packages' requirements for the repository updated with
information about required packages' dependencies. And new page with
information about xUbuntu 21.10 repository created.

From under-the-hood, the page got some style updates, mostly related to showing
inline and blocks of code. Now it should look a bit better. :)
