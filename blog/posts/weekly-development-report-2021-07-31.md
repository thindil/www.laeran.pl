-- layout: blog
-- title: Weekly development report 2021-07-31
-- filename: blog/posts/weekly-development-report-2021-07-31.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Referring to the previous week post: now I know what I was missing in the
stable version of the game: not working renaming for modules and crew
members. ;) Ok, these are fixed now, same as showing info about the overloaded
ship. This mean, in around 24 hours since this post a new, again more stable
version of the game will be available to download.

In the development version, not too much visible things done in this week:

* The problems found in the stable version are now fixed in the development
  too.
* Fixed showing info about taken cabins on the list of available missions in
  bases.
* Also, fixed problem with scrollbar on the know bases list. It didn't reset
  correctly after reenter the knowledge screen.
* Most of the week was spent on playing with sorting various lists in the game.
  I wasn't satisfied with the first way used to solve the problem, so I tried
  a few different solutions. And I think that I finally found something. :)
  All the existing sorting code was updated to the new version, also I've
  finished work on sorting the crew members inventory.
* Started work on updating the debug window. It was looking awful. Now it
  should look just bad. :) Some work left here to do.
* Fixing problems reported by AdaControl and generally made the game code
  looks a bit better. Standard. :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The work on `Tk.Winfo` package is done for now. All bindings, their
documentation and unit tests are on their places. Especially work on
documentation was done in this week, but also there were some changes to the
bindings too. Also, I've fixed all problems reported by the AdaControl tool.
Now the work started on bindings for Tk **ttk::entry** widget and its commands.
For now only creating and configuring the widget code is ready. Work started on
various commands related to the **ttk::entry**. And added a few unit tests for
the bindings.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The work on the console version of the program (at least it's the first alpha
version) is slowly ending. There left only a few things to do and let's hope in
the next week, there will be finally a new release of the project. For now, in
this week were done:
This time I can write that the work on console version is very close to the
end. Finally. :) But referring to the last week report: no new release in this
week was done yet. Things which are finished this week:

* Almost finished work on manipulating content of the system Trash. Only one
  thing left: deleting the selected files and directories from the Trash.
  Restoring, clearing the Trash should work now.
* Updated included the program's module for support for my other project, Bob.
  Now it works only in the graphical version of the program. Console version
  doesn't have yet full support for the program's modules.
* Updated the project documentation with information how to build the console
  version of the program.
* Also, related to the project documentation: added information about coding
  standard which I should use in the project, plus info about testing
  procedures used by the project.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

I could literally copy and paste report from the last week: fixing the problems
reported by AdaControl and adding the unit tests to the project continues. The
only change is that adding unit tests is almost finished. Thus, in the next
week, the report here should a little different, but still very short. :)
