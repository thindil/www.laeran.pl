-- layout: blog
-- title: Weekly development report 2021-07-10
-- filename: blog/posts/weekly-development-report-2021-07-10.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This week everything back to normal.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

I could now almost copy and paste the report from the last week about the
stable version. A few days after the last release, I found that setting reward
for missions in bases doesn't work properly. Also, one more type was hunted
down too. But, both have to wait a moment. This Sunday belongs to the
development version. Well, maybe in the next week I will find another bug
too. :)

And about the development version:

* Some small changes to the game statistics screen made. They are under the
  hood, so the screenshot from the last week is still valid. The only visible
  change there is now all lists have their tooltips.
* Started and finished work on the new version of the available missions list
  in bases. Now it presents [more information](https://imgur.com/3cWRvWd) about
  each available mission, and it looks similar to the rest of the UI. I think
  this is the last part of redesign UI work. Now, the work on the UI will go in
  a different direction.
* Another week with another bugs fixed and probably even more added to the game.
* The fun with fixing problems reported with AdaControl very slowly moving
  forward. At this moment it is checked around 1/7 of the whole code. And the
  checking takes now 4 times more time than compiling the release.

And as mentioned above, it is time for the new development release of the game.
In less than 24 hours since this post, a new, shiny, development version will
be available to download.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The report this week is a bit short. The work on the new demo program for the
library for now is done. It is a very simple calculator, which should works
and even calculating the proper results. :) This work took almost the whole
week. After that, I started again adding various bindings. This time they are
for Tk **winfo** related commands. The new package is created, even a few bindings
added, but still a lot of work to do. Also, started work on unit tests for
the `Tk.Winfo` package.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week brings a bit more new things to the console version of the program
than previous weeks.

* Finished work on setting the user defined commands in console version of the
  program. Now it is also possible to delete commands.
* Added option to view and enable or disable the program's modules in the
  console version. This mean that the program's configuration is now also
  finished in the console version.
* Started work on using the user defined commands in the console version. For
  now it is possible only execute the selected command, it still not showing it
  result in the program.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

This week the only change to the previous week report is that I finally started
fixing problems reported by AdaControl in the `Layouts` package. But everything
other is the same: the `Config` package looks good for AdaControl and the
program's code now has a bit more pre and post condition checks. This one work
is done for now.
