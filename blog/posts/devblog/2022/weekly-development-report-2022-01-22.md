-- layout: default
-- title: Weekly development report 2022-01-22
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. Looks like I'm almost finished changing my
development toolchain. It is mostly now moved to the separated jail instead of
virtual machine. There is still some small work to do, but the most things
work same as earlier.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The last week of preparation for the next big stable release finished. As
usual, the most problems found in the last minute checks, mostly related to
the shipyard type of bases. Anyway, still better than a day after a release.
:) There are still some small fixes to do before release, but everything
should be ready on time.

* Again, a lot of the code refactorings and, generally, making it look better.
  It triggered some bigger changes to the code too. And to some unit tests, as
  usual. At this moment, it looks like it doesn't add any new bugs.
* Added limit for maximum amount of mobiles prototypes which can be declared
  in the game data files. The limit is, I hope, high enough, that nobody hit
  it too fast. Of course, the game's modding documentation updated too with
  more information about the limit.
* Added blocking “Install” button in shipyard when installation of the
  selected module is impossible. Also, the button now change its text to short
  information why installation blocked. Additionally, added the tooltip to the
  button with more detailed information about lack of requirements for
  installation of the module.
* Fixed installing armor on the player's ship when there are is maximum amount
  of installed modules. An armor shouldn't be counted to the limit. It is
  enough that it is a unique module.
* Added information that the selected module is unique to the module's
  description in shipyards.
* Fixed blocking “Install” button when there is no free turret during
  installing a gun or harpoon gun.
* Probably fixed, will need tests, the game should now work with a bit older
  Linux versions than earlier. Still may not work with old stable Debian or
  CentOS 7, but even this bug is slowly going to be fixed.

And as mentioned at the start. In around 24 hours since this post, a new big
“stable” version of the game will be available for download. Then again, the
work will back to updating the UI. :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This time copy and paste from the previous week. The whole week spent on fixing
the problems reported by `gnatprove`. And updating the unit tests to the new
version of the code.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous week. Thus, almost the same
report as the earlier:

* Finished clearing the code of the console version of the program. This time
  mostly related to various dialogs.
* Added closing the *about dialog* in console version with Escape key. This
  triggered some changes to the code for better detection of the user's pressed
  keys. Now this *unique* option is slowly added to the other dialogs too.
* Added option to move around the *about dialog* in console version with left and
  right arrows keys too.
* Another small, but I think helpful change: Enter key now accepts entered
  command in Execute With dialog in console version.
* Fixed crash in console version when trying to open the project's website when
  `xdg-open` script isn't installed.
* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. Removed here the last line, so some things are
  changed. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The most of the work this week spent on refactoring the project code. But a few
new features added too:

* Code related to the shell's aliases, history and writing output to the
  console moved to the separated modules. Now the code should be a little more
  readable. This work took the most time in the week.
* Added command to adding new aliases to the shell. It still needs some
  polishing but generally works good.
* Updated the in-shell help with information about the new command.
* Started using the constant `maxInputLength` to set the database fields. As
  the user can't enter longer text into shell, there is no need to have longer
  fields in the database.
