-- layout: blog
-- title: Weekly development report 2021-05-29
-- filename: blog/posts/weekly-development-report-2021-05-29.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Looks like typos in the stable version will have to wait one more week to
release. I also found a few problems with setting various keyboard shortcuts,
and I'm slowly fixing them all. Well, at least the next version will be a bit
more stable than I expected. :D Plus a few more typos were found and fixed
too.

The development version is going forward as usual. As someone said: "Ada code
printer" :P Most of the work in this week were done under the hood, but some
visible changes also incoming.

* Started work on redesign of the crafting screen. Most of the work is done,
  but for now it is a mix of old and new UI thus no screenshot today yet.
* In-game help, mostly the First Steps section got some update and
  clarifications.
* Fixed the same problems with setting keyboard shortcuts which were found in
  the stable version. And typos.
* Started work on clearing the code related to the in-game dialogs.
* And continue work on code cleanup and generally making it better.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Finished renaming subprograms in `Tcl.Info` package. Now they have the same
style for names as in the other packages. Unit tests for the `Tcl.Info` were
updated either. Same with the subprograms in packages `Tk.TtkWidget` and
`Tk.Grid`. Also, their unit tests were updated too. Then started updating the
code documentation (more information about the enumerations options, etc.) in
packages: `Tk.Menu`, `Tcl.Info`, `Tcl.Variables` plus cosmetic updates to
their unit tests. Fixed code documentation for packages `Tk.Labelframe`,
`Tk.TtkLabelFrame` and `Tk.TtkFrame`. Also, started experimenting with debug
mode for the library: when enabled, it shows executed Tcl commands in console.
I'm still not sure about it, thus we will see if it stays in the library or not.
At the end, I started work on binding for Tk **image photo** commands.
From the project organization: fixed AdaControl GitHub workflow to trigger on
code committing.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week, bring one new things to the console version of the program:

* The dialog about the program in console version is finished: it shows the
  same information as in graphical version: link to webpage, list of
  programmers and translators, etc.
* In both versions of the program, fixed showing content of directories after
  entering them. Sometimes earlier it was showing content of different
  directory.
* Also in both versions: looks like finally fixed crash in the program which
  sometimes happened on auto refreshing the current directory information
* And started work on setting the program options in the console version. At
  this moment it is very early work, thus nothing is ready yet.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl.

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Standard header here: work on fixing the problems reported by AdaControl slowly
moves forward. But also, a few typos and grammar problems were fixed in the
documentation for the configuration file and fresh, empty pages. And added
creating another meta link: this time with information about the author of the
page. It can be set or per page or get from the website configuration file.

### [tkGruvbox](https://www.laeran.pl/repositories/tkgruvbox)

*Tcl/Tk and TkInter theme based on Gruvbox color scheme (written in Tcl)*

Something new this week. Freshly started Tk/TkInter theme project which is
based on the [Gruvbox](https://github.com/morhetz/gruvbox) color scheme and my
previous Tk theme TkBreeze-dark. Same as previous theme it uses images for
buttons and various other UI elements. Additionally, this repository is mirrored
on [GitHub](https://github.com/thindil/tkgruvbox) and [GitLab](https://gitlab.com/thindil/tkgruvbox).
