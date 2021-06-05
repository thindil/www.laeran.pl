-- layout: blog
-- title: Weekly development report 2021-06-05
-- filename: blog/posts/weekly-development-report-2021-06-05.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version, problems with setting keyboard shortcuts were fixed,
and I finally found the problem with giving items to the crew members from
the player's ship cargo. It is fixed now too, thus in around 24 hours since
this post a new, a bit more stable version will be available to download.

In the development version, works almost as usual. Same as in previous week,
the most work were done under the hood, but some visible changes are available
too:

* Redesign of crafting screen is almost done. For now, it has all abilities
  of the old version, but I want to make it a bit more user-friendly. Thus
  still no screenshots available here.
* Same as in the stable version: now setting keyboard shortcuts should work
  properly. Plus one crash less during giving items to the crew members. :)
* A lot of code cleanups related to the in-game dialogs. Also, I found a few
  dialogs without header yet. Now they are fixed too. And a few dialogs were
  displayed incorrectly after changes - they are fixed now too.
* Standard footer here: fixing problems reported by AdaControl - static code
  analysis tool. This week it also triggered some work with updating unit
  tests.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This week the main focus was on creating bindings for Tk **image photo**
commands. At this moment the specification of the package is done, now work
started on writting the code for bindings. Also, added stubs for the unit tests
for the `Tk.Image.Photo` package. From the other work: the experiment with
debug mode for the library wasn't successful, thus the whole code related to it
were removed. Package `Tk.Widget` got subprogram `Option_Image` for options
which value is `Positive_Float` type. `Window_Position` record from `Tk.Wm`
package was renamed to `Point_Position` and moved to the `Tk.Widget` package.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week, some project organization were done, also the work on console
version of the program slowly moving forward. But generally, not too much to
report:

* Added Tcl script to run AdaControl checks. It is recommended to use Docker
  image for it, with GNAT FSF version 9.3.
* Continue work on setting the program in console version. At this moment, only
  the main program options user interface were added, still the most work
  before me.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl. Some things probably never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Standard header here: work on fixing the problems reported by AdaControl slowly
moves forward. Finished work related to adding author meta tag to the websites.
Now documentation about it should be done too. Also, added another meta tag to
the generated pages: description (tag which appears mostly in search results in
search engines). It can be also set globaly for the whole website (a new
setting in the global configuration file) or separately for each page. How to
do it is explained in the user documentation of the project.

### [tkGruvbox](https://www.laeran.pl/repositories/tkgruvbox)

*Tcl/Tk and TkInter theme based on Gruvbox color scheme (written in Tcl)*

In this week, two other variants of theme are added: same as before, light and
dark version but this time, much simpler themes, without images but based on
standard *Tk* theme **clam**. For now it is end of the work on this project,
unless someone has any ideas or problems with it. In that situation, feel free
to contact with me. :)
