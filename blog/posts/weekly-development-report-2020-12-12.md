-- layout: blog
-- title: Weekly development report 2020-12-12
-- filename: blog/posts/weekly-development-report-2020-12-12.html
-- Author: Bartek Jasicki
Welcome to the weekly development report or what was done in my Open Source
projects in the last week. This time, the introduction will be a bit longer. At
the beginning of the week I (finally) discovered [Fossil SCM](https://www.fossil-scm.org/).
And I felt in love almost on first sight. I have to write, it fits exactly what I
wanted from the version control system. It is distributed but can be used also
in that same way like centralized VCS (like Subversion or CVS). It has all
needed by me options without all complication of Git. Also, it is very easy to
install (also on server), allows controls all repositories in that same moment
and have build-in web UI. I think that Fossil better suit my needs: Git was
created to maintain large repositories of code maintained by many people (like
the Linux kernel). Fossil was designed to be self-hosted (it should work even
on free web hosting), easy to maintain even by one person and for manage many
small projects at the same time. Of course, it is still our honeymoon thus
probably I'm a bit biased toward Fossil. But I really start liking to have
searchable source code repository with searchable documentation plus ability to
maintain server and community even off-line. The decision about the change of
version control triggered of course a lot of work in all projects. At this
moment I'm probably at the start of the work in switching from one system to
another. When I finish the work I will write about the whole journey here
on the blog. Now, back to the more detailed information.

### [Steam Sky](https://thindil.itch.io/steam-sky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version of the game the quiet strikes back again. Not sure if it
is a good or a bad sign. :)

In the development version as usual work on UI continues. And continues. And
continues...

* Finished (at least for now) work on the game dialogs. Now all looks that same,
  also they are not that intrusive as they were.
* Removed not used settings from the game. For now there are no animations yet,
  thus the old setting for them was useless.
* From small things: now the game map can be zoomed in and out with mouse wheel.
* And main work in this week: started redesign of ship to ship combat UI. It
  [current state](https://imgur.com/FRUBOqn) versus [old state](https://img.itch.zone/aW1hZ2UvNDkxMTgzLzM0NjQxMDEucG5n/original/9d3u1c.png).
* Also, as usual, some bugs were fixed and probably some others introduced to
  the game. Same, code refactoring and updating it documentation work continues
  too.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

Finished work on Ada binding for Tk `grid` command. And started work on the
documentation for it. Fixed setting Tcl interpreter for them too. Also, TASHY2 as
the first project was moved to Fossil repository. The first stage of the
switching is finished now. Some files were moved to the project documentation.
The old [GitHub repository](https://github.com/thindil/tashy2) will still be
updated but the whole development and support was moved to Fossil. Also,
added another mirror of the repository on [GitLab](https://gitlab.com/thindil/tashy2).
This one is fully automated.

### [Hunter](https://github.com/thindil/hunter)

*Graphical File Manager for Linux (written in Ada)*

Unfortunately, due to switching other things to Fossil, work on Hunter was very
limited this week. Mostly translations were fixed and cleaned. The biggest
change was adding path buttons to the Trash. Also, started work on code
reorganization, related to the bigger project which "soon" will be started
here.

### [TASHY](https://www.laeran.pl/repositories/tashy)

*Ada binding to Tcl/Tk, based on TASH*

During usage of the library I was find that binding for Tk commands `lower` and
`raise` not work properly. Thus, at beginning of the week I started fixing
them. Of course, every solution cause new problems :) I found that code can be
cleaned a bit. And started working on it. When I finished moving TASHY2 to
the new home, I started moving TASHY too. At this moment this work is not
finished yet, but same as for TASHY2: the old [GitHub repository](https://github.com/thindil/tashy)
will still be updated but the whole development and support will be moved to
Fossil. Also, added another mirror of the repository on [GitLab](https://gitlab.com/thindil/tashy).
This one is fully automated.

### [www.laeran.pl](https://www.laeran.pl/repositories/page)

*Yass project to generate this website*

That maybe not a real Open Source project but probably if someone is looking
for an example how to set up own Fossil repositories can check there. Of course
here also was done a lot of work related to the moving the code projects to
their new home. Mostly by testing some possibilities how it should look :)
Also, the old [GitHub repository](https://github.com/thindil/www.laeran.pl)
will still be updated but the whole development and support will be moved to
Fossil. Added another mirror of the repository on [GitLab](https://gitlab.com/thindil/www.laeran.pl).
This one is fully automated.
