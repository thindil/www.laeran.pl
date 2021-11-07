-- layout: blog
-- title: Weekly development report 2021-04-24
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

As usual, the big release was a great success... in finding bugs. :)
More seriously, definitely success and much better than the previous version.
I got some nice feedback too. Thank you very much everyone. :)

And back to the report: the stable version has become a bit more stable. I
squished a few bugs in this week, thus as usual, in around 24 since this post
a new minor stable version will be released. And I still have a feeling that
the next minor release is around the corner.

The development version report is very similar to the stable version:

* Fixed all the same bugs which were found in the stable version.
* Started work on update the game options UI. There are going mostly cosmetic
  changes. At this moment it is still work in progress, thus no screen this week.
* Some project organization work, mostly related to the fact that now the
  whole code of the game (stable and development versions) are in Fossil and
  uses GitHub workflows for checking the code.
* Almost never-ending story called code cleanup and making it generally
  better: fixed some problems reported by AdaControl tool and cleaned up a bit
  of the UI related code.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The new binding, for Tk command **image** was added as `Tk.Image` package. Of
course, unit tests for them are also on their place. Added binding for
Tcl_Merge as `Merge_List` to `Tcl.Lists` to merge a few strings into Tcl
list. And then returned to adding the binding for various Tk **wm** commands.
Also, added some unit tests for them. Some code cleanup were done too.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

As usual, a bit "lazy" week in the development, mostly the maintenance work:

* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl.
* Fixed showing or hiding cursor in console version of the program, mostly
  related to the setting files and directories default program option.
* Finished work on setting default associated program for files and directories
  in the console version.
* Started work on scrolling preview of text files in the console version. For
  now only scroll line by line works. Plus there are a few problems to fix.

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

And same as with the other projects, the fun with fixing the problems reported
by the AdaControl has started. This was the main activity in the project in
this week. Also, fixed showing crash traceback on Windows. Plus, again, some
work not directly related to the code: updated the project README.md file with
information how to build it with Docker image and generally made it more
friendly for English grammar. :) Also, fixed GitHub workflow for AdaControl.
