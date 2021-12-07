-- layout: default
-- title: Weekly development report 2021-06-12
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable branch, a new version was released. A few quiet days passed and
of course I had to find a couple of typos. Again, no crashes noticed, thus if
you got one, please report it to me. It also means, that I will wait one more
week to check what else I can find in the game. :)

In the development version, work going forward as always:

* Finished work on redesign of the crafting screen. Now it by default
  [showing](https://imgur.com/E1wNNtZ) info about missing workshop, tools or
  materials. Also, added there an option to search through recipes names.
* Because there were a few weeks without screenshots, in this week will be
  another. :) The screens for buying recipes, healing wounded crew members and
  [buying repairs](https://imgur.com/iKHcAii) in bases were redesigned too.
  They now not only looks  similar to the other in-game screens, but also
  presents by default more information.
* As usual, some invisible work were done too. At least, one of these tasks
  was finished, thus I expect that now I will have a bit more time for doing
  more "visible" changes. :)
* A few bugs were fixed, and probably a lot more new added to the game.
* Some small changes to the project organization: be sure that GitHub workflow
  uses the proper version of tools to build the game, etc.

And as the another four weeks passed since the last development version, time
for another release. :) Around 24 hours since this post, a new version will be
available to download.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Almost the whole week was spent on adding various bidings for Tk **image
photo** commands. Most of them are present, same as unit tests for them. Now I
"just" need to add the code documentation and check everything is proper. From
the other work here: another `Option_Image` procedure arrived to `Tk.Widget`
package, this time for `Point_Position` type. Additonally, added `Option_Image`
for switch-like options (options which are or just present or not added to the
widgets configurations). Of course, that subprograms got unit tests too.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This week was almost complete copy of the previous week. Just the report will be
even shorter than the ealier:

* Continue work on setting the program in console version. All the main
  program's options are on their places, it is possible to traverse through
  them, but at this moment only a few of them can be set.
* Also, updated GitHub workflows to use exact version of the Docker images used
  to test and build the program.
* Standard, copy+pasted from the last weeks: a lot of work with fixing problems
  reported by the AdaControl. Some things probably never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

And we very slowly move forward here with fixing the problems reported by
AdaControl. At least work started on `Config` package. :) This week also was
done some work in the project organization: added a Tcl script to execute
AdaControl tests in Docker image. In the program code, here landed the last
expected change: the default layout got standard meta tag *viewport*. This one
isn't configurable, thus no changes inside the existing projects are needed.
The project documentation was updated for changes either.

### [Docker Ada](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

And special quest this week: the big change to all images: all of them were
updated to GNAT version 10.2. These images which were based on Ubuntu 20.04
were updated to version 21.04. Also, *AdaBuild* and *AdaBuildWin64* images got
updated all included libraries. Another big change to these two images is fact
that they now are based on base images not related to Tashy. Of course, they
still contains the same libraries, just now Tashy is build inside of them. And
one information: if you want to use *AdaBuild* image for check your code with
AdaControl, it is recomended to stay with the previous version based on GNAT
9.x. At this moment it is probably all in this project.
