-- layout: default
-- title: Weekly development report 2022-02-05
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. As with the new month, two more projects are
archived on GitHub and GitLab as I don't plan to work on them in the nearest
future: tkGruvbox and YASS.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And another two small bugs found in the stable version. Fortunately, same as
in the previous week, they are mostly cosmetic issues, thus shouldn't be too
annoying. :) I better will wait one more week, to check other things, before
prepare a new, a bit more stable release.

In the development version, the work, same as in previous week, mostly focused
on adding new icons to the game:

* Added a few new icons to the game, and updated existing ones, to be more
  visible (mostly by changing colors). At least this week is something to
  [show](https://imgur.com/p3QviPS). That is not only a visual change. The new
  icons are vector graphic images, while the old ones were a font. This
  trigger some changes to the game theming code too. That is the main reason
  why everything is going so slow.
* The changes in icons also triggered changes in the game documentation, in
  modding guide exactly. It should be now updated to the new version of icons
  too.
* Technobabble: some code refactoring, as preparation for apply formal
  verification of the code.
* Standard under-the-hood work: code cleanup and generally making it
  conformant with my own coding style. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

As mentioned in the previous week, the project is now the second the most
important here for me. :) Thus, there is also some work done. This week focused
mostly on adding various configuration options to the shell.

* Added option to set the maximum amount of the shell's command's history
  entries.
* Added command to show all available subcommands for the `options` command.
* Added help for various subcommands related to the shell's configuration
  options.
* Added type of value to the shell's configuration options and showing it in
  the command `options show` output.
* Added better exceptions handling. Now it should show a lot more info than
  earlier.
* Added default value for each the shell's configuration's option and showing
  it in the command `options show` output.
* Added command `options reset` to reset value of the selected configuration's
  option (or all of them) to their default values.
* Added help related to the command `options reset`.
* Added configuration option to enable or disable saving invalid shell's
  commands to the shell's history either.
* Some code refactoring: added pragmas to various procedures and functions,
  mostly related to the shell's options. Also, some code reorganization, like
  move all shell's command history database related things to the one
  procedure.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This time copy and paste from the previous week. The whole week spent on fixing
the problems reported by `gnatprove`.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Continuation of the work started in the previous weeks. Thus, almost the same
report as the earlier:

* Added closing the *delete dialog* and *rename items dialogs* in console
  version with Escape key.
* Added accepting the user entry with Enter key in *rename dialog*  in console
  version.
* Added better counting size of the available programs' menu when setting the
  default application for the selected item in console version.
* Standard, copy+pasted from the last weeks: some work with fixing issues
  reported by the AdaControl. Removed here the last line, so some things are
  changed. :)
