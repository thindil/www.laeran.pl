-- layout: default
-- title: Weekly development report 2021-01-02
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html
At the start: happy new year for everyone :) Let's hope this one will be better
than the old. Now, back to the routine.

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

This week work was completely focused on the development version of the game.

* Generally, the most of the work this week was done on trade screen redesign.
  It is "almost"  done, but some polishing is required. Thus, no screenshots
  this week.
* As almost always, some small code tweaks, mostly related to the code
  documentation were done too.
* A few bugs were fixed and probably a few new "features" added.

But the main change to the project this week is related to its organization.
Long story short: the game has the new development home. It not only moved
from GitHub to my server. It also changed version control system from Git
to [Fossil](https://www.fossil-scm.org/).

By a long time I was using Git as my main VCS. I was aware of existing a few
alternatives like Bazaar or Mercurial but none of them was interesting for me.
Around one month ago I discovered another alternative: Fossil. After reading
its documentation and some small tests, I felt in love to it. :) Its commands
are very similar to these used in Git, thus migration isn't too hard for
muscles memory. But Fossil was designed for managing small projects, when Git
was created for support creating the huge project called Linux. Also, Fossil
is a lot smaller (especially on Windows and macOS) than Git. Plus, the best
things: it has build-in web UI, is deadly easy to deploy on a server and easy
to set up. Even on a free web hosting :) The whole observations about the
Fossil SCM deserve a separated blog entry, which probably soon or later I will
write.

By the earlier month I was slowly moving my other projects to Fossil from Git
and in this week I finally moved Steam Sky too. Not everything was done
perfectly, for example the stable version of the game is still hosted on
GitHub. But I'm still much happier with Fossil than with Git. It makes the
project management a much easier: having everything in one place, even the
development forum is a very nice feature. Plus, I started thinking about using
Fossil even as the main page for the game: it is very cutomizable and uses a
lot less resources than any common solution like WordPress or phpBB. But this
is still food for thoughts. The link to the source code was also updated thus,
everyone can see how it looks now :)

Generally, as Steam Sky was always an experimental field for me with some
programming related technologies, now it is a unique project: not only written
in Ada and some parts even in Tcl, but also stored and managed by Fossil :D

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

This week was mostly designated to creating the project's unit tests. And
fixing all problems which they are detected :) Tk_Widget package is for now
tested, and started work on unit tests for Tk_Button. Also, here is a new Tcl
binding for command `info exists variable` of course with added unit test for
it too. More bindings for command `info` will be added later.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

Finally, finished moving packages to the proper directories. The code
documentation got some updates either. Also, added some labels to a few loops
to make the code more readable. And at the end, started work on the main
feature of this release: a console version of the program. At this moment I
mostly remind myself how to use ncurses library. But some, very small work in
the project organization and started work on the program menu in console. Also,
the project page got some work: added About page plus some documentation
cleanup.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

All changes to the page are invisible for humans. Only small correction to
setting default viewport for the page and added meta tag with information about
the author of the page. Also, the project page got small lifting.

### [Docker Ada](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

AdaBuild was updated with adding Ada binding for the ncurses library. It was
needed for the new version of [Hunter](https://www.laeran.pl/repositories/hunter).
Also, documentation of the project got some updates. Now it should be easier to
find the list of available Docker images.
