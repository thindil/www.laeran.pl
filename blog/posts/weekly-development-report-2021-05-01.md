-- layout: blog
-- title: Weekly development report 2021-05-01
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

As usual, again the day after the release new bugs in the stable version were
found. Fortunately, this time only "cosmetic" things, no crashes yet. Probably
I'm missing something. :) Anyway, the hunt for bugs continues here, still a
few of them on the radar.

The development version slowly moving forward:

* The bugs found in the stable version were fixed here too.
* The work on redesign [the game options](https://imgur.com/SlUwayo) is
  finished.
* As one player suggested during release: added option to set which mouse
  button use for in-game menus. By default, it is still left, but can be
  changed to the right button.
* The knowledge screen got small tweaks to look, mostly added some padding
  between various elements.
* As usual, technical stuff: some code cleanup for UI code were done and a few
  problems reported by the static analysis tool were fixed.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This week brings a lot of new bindings for a few Tk widgets. `Tk.Frame` as a
binding for Tk command **frame** is made. Also `Tk.Toplevel` package was
redesigned as a child for `Tk.Frame`. Added another child for `Tk.Frame`,
`Tk.Labelframe` which brings bindings for Tk command **labelframe**. Binding
for command **ttk::frame** are now in the package `Tk.TtkFrame` and binding for
command **ttk::labelframe** is in its child package `Tk.TtkLabelframe`. Also
added new type `Anchor_Directions` to `Tk.Widget` and `Option_Image` and
`Options_Value` subprograms. And of course, unit tests for all the new
subprograms were done too. Now the work is back to the binding for Tk command
**wm**.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The main feature this week is finished preview of text files in the console
version of the program. Additionally, the program got some other work:

* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl. Again, this took the most time in the week.
* Added elipsizing of long file and directories names when confirming deleting
  them.

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Fun with fixing problems reported by the AdaContol continues. And will continue
by some time. :) Second thing, some user documentation should be now more
English grammar friendly. Also, changed the name of GitHub continuous
integration workflow.
