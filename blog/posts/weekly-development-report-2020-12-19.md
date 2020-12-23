-- layout: blog
-- title: Weekly development report 2020-12-19
-- filename: blog/posts/weekly-development-report-2020-12-19.html
Welcome to the weekly development report or what was done in my Open Source
projects in the last week. The work on moving my Open Source projects slowly
going forward. Another two repositories are migrated from Git to Fossil. But
this time more was done inside the projects presented below.

### [Steam Sky](https://thindil.itch.io/steam-sky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version: peace and quiet. As usual, I probably miss something :\]

In the development version at this moment, finished work on the new ship to
ship combat UI:

* Destroyed modules on player's and enemy's ships are now better visible
* Redesigned [assigning](https://imgur.com/E7pVBK2) the crew members to the
  boarding party
* Also, information about the boarding party was moved to the general
  information about the player's ship crew (as showed on the image above).
* (Finally) added option to assign also defenders on the combat screen.
  Earlier it was requiring to go to the crew info screen. For looking who is
  assigned too. Now, everything is in one place.
* Started work on update the boarding combat screen. At this moment there not
  too much to show yet.
* Also, as always, signature: some code were refactored, some code
  documentation updated, some bugs fixed, many new added :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The documentation for the `grid` Tk command should now be finished. The work on
the `toplevel` widget binding was finished either. Started adding the
documentation to its code. The biggest change this week to the existing code
was change type of Tk\_Widget from Integer to proper System.Address. I'm a bit
surprised that it was working earlier (demo was compiled and run without any
problems). Anyway, now everything should be as expected and that change isn't
visible from the outside of the library. Also, fixed generating unit tests.

### [Hunter](https://github.com/thindil/hunter)

*Graphical File Manager for Linux (written in Ada)*

Due to a lot of work with the other projects, there were a small amount of
changes in Hunter this week. Only work on the code reorganization slowly moving
forward.

### [TASHY](https://www.laeran.pl/repositories/tashy)

*Ada binding to Tcl/Tk, based on TASH*

The project is fully moved to its new Fossil home. There were some code
refactoring inside the binding and the documentation were moved to the new
places. And because everything works properly again, the new, shiny version of
8.6.11 was [released](https://www.laeran.pl/repositories/tashy/wiki?name=Download).
The Docker images are upgraded too. At least one thing done this week :)

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

Old page with information about Ada Matrix room was removed as unneeded (the
room was changed it profile). In exchange here is a new page with information
how to support us (me and my page :)). Also, updated information about the Ada
Search page. The page itself also was updated with the new version. The main
page of the website got some small cleanup. There is still some work to do, but
it should be finished in next week.

### [AdaSeach](https://www.laeran.pl/repositories/adasearch)

*Custom Google and searchcode search engines for the Ada/SPARK programming
language*

This project for now was only moved to the new [Fossil](https://www.laeran.pl/repositories/adasearch)
repository. Nothing new in the code. Also, the old [GitHub repository](https://github.com/thindil/adasearch)
will still be updated but the whole development and support will be moved to
Fossil. Added another mirror of the repository on [GitLab](https://gitlab.com/thindil/adasearch).
This one is fully automated.

### [DockerAda](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

Same as *AdaSearch* above: the project for now was only moved to the
new [Fossil](https://www.laeran.pl/repositories/dockerada) repository.
Nothing new in the code. Also, the old [GitHub repository](https://github.com/thindil/dockerada)
will still be updated but the whole development and support will be moved to
Fossil. Added another mirror of the repository on [GitLab](https://gitlab.com/thindil/dockerada).
This one is fully automated.
