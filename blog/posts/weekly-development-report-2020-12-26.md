-- layout: blog
-- title: Weekly development report 2020-12-26
-- filename: blog/posts/weekly-development-report-2020-12-26.html
-- Author: Bartek Jasicki
Welcome to the weekly development report or what was done in my Open Source
projects in the last week. In this week only one project (Hunter) was moved
to the Fossil, but with some problems. More details are below.

The most important thing: happy holidays everyone :)

### [Steam Sky](https://thindil.itch.io/steam-sky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Because it is the last entry in this year, time for some summary of what
happened in the game in the last year.

* In May was released the new, big stable version, 5.0 of the game.
* Also, I've made the decision to change the library used by the game from GTK
to TK. This was resulted in a bit longer than usual wait for the first
development version of the game. And a lot more buggy than usual :)
* Anyway, the work towards the next big stable version, 6.0 slowly continues
which should bring mostly refreshed UI plus some changes invisible for the
players.
* In this same time as usual, the stable version became a bit more stable with
a few additional releases.
* On itch.io was added an option to download the development version too.

There will be one big organization change related to the game development in
this year, but it will be announced probably after New Year. But no worries,
the game is and will be free and on this same GNU GPLv3 license as now. :)

And now time for the standard weekly report:

The stable version again is quiet. Everyone probably waits until I finally
start fixing all these typos and grammars which I should see. :)

In the development version, the whole week was dedicated to the work on the
combat interface.

* There were fixed some bugs related to the combat.
* Finished work on ship-to-ship combat. That it [looks now](https://imgur.com/MlZq0oX).
* Also, almost finished work on the boarding combat interface. There will be
some changes very soon, but I think it looks [better](https://imgur.com/KfJvZC5) than earlier.
* Same as by the last few weeks: some changes invisible to the players are
done too.

And probably the most important information about the development version:
because since last release  4 weeks has passed, time for another development
release :) In around 24 hours since this post a new, shiny, buggy, development
version will be available to download on [GitHub](https://github.com/thindil/steamsky/releases) and [itch.io](https://thindil.itch.io/steam-sky).

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The documentation for the binding to Tk command `toplevel` was finished. The
almost empty package Tk.Menu was added only with type for Tk `menu` widget. In
the Tk.Widget package there was added a new type Tk\_Window as pointer to the
Tk windows. The `toplevel` command binding got update its options types `menu`
and `use_container` to proper Tk\_Menu and Tk\_Window types. Also, added
binding to get the pointer for the Tk windows. The end of the week was spent on
creating unit tests for Tk.Widget package. Of course, a few bugs in the binding
were found during this stage.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Due to a lot of work with the other projects, there were a small amount of
changes in Hunter this week. Only work on the code reorganization slowly moving
forward. The biggest change this week was move the development code of project
to the new [Fossil](https://www.laeran.pl/repositories/hunter) home. As it was
the first project which I was moving with branches, unfortunatelly not
everything was moved properly. The old stable and GitHub page branches got
changed names. Now I know that before migration to Fossil I need to migrate
only one branch, not everything :) Anyway, everything is now in it new home and
there are available mirrors on [GitHub](https://github.com/thindil/hunter)
and on [GitLab](https://gitlab.com/thindil/hunter). This one is fully
automated.

### [TASHY](https://www.laeran.pl/repositories/tashy)

*Ada binding to Tcl/Tk, based on TASH*

Just small update: added GitHub action to automatically close all pull
requests there.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

The most visible change this week is a new color theme of the page :) It was
changed to match the repositories style. It should now look a bit better.
Also, Ada Search page was fully integrated with the site: also previous
directory was replaced by just HTML file. On Support Us page, the buttons were
removed as they only slowed loading the page. The website privacy info was
updated with information about the repositories. Contact page got a few new
options how to contact with me. Under the hood the page header was moved to
separated layout file and all pages got canonical URL settings. I think it is
enough changes for now for the page, thus work here is finished for now.

### [Ada Seach](https://www.laeran.pl/repositories/adasearch)

*Custom Google and searchcode search engines for the Ada/SPARK programming
language*

Added a new search engine to the project: [searchcode](https://searchcode.com/).
It is the search engine focused on searching through various Open Source
projects code in the most known public repositories on the net (like GitHub,
GitLab, etc). It is tailored to return only results related to the Ada
programming langugage. Also, fully finished moving the code to the [Fossil](https://www.laeran.pl/repositories/adasearch)
repository by moving there all the project documentation. Here work for now
also finished.

### [Docker Ada](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

AdaBuild and AdaBuildWin64 images were updated to the newest version of Tashy
images. Same as with Ada Search: fully finished moving the code to the [Fossil](https://www.laeran.pl/repositories/dockerada)
repository. And a few typos and grammar problem were fixed too. For now, it is
all what was to do in this project.
