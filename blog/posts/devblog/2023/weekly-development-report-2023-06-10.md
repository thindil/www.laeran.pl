-- layout: default
-- title: Weekly development report 2023-06-10
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Again, the stable version doesn't want to cooperate and doesn't report its
bugs. ;) No changes here in the last week.

The development version finally has something to show. Not too much, especially
if compared to the amount of work which it took, but still something. :) Plus
the standard tasks from the previous weeks (and months):

* As mentioned in the previous week's post, I shifted focus to updating the
  dialog with information about the player's ship's modules. And finally, the
  work is done here. Of course, there is still room for improvements, but that
  is for later. ;) Promised something to show: [the new look](https://imgur.com/dIRRRyw)
  of a cabin's information, and [the old one](https://imgur.com/1YebHVy).
* Started work on presenting some more information about the player's ship's
  modules on the modules' list. Here is still some work to do, so no screens
  yet. ;) But I hope to finish this work in the next week. It requires a lot
  less changes in code compared to the previous task.
* Some parts of the code are moved to Nim too. With tests, etc. Now, most code
  related to bases should be in Nim.
* Usual footer: the remaining Ada code got some improvements too.

And because the previous development version of the game was almost four weeks
ago, time for the new one. In around 24 hours since this post, it will be
available for download.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

Another big week for a small thing. ;) Nimalyzer got a new, still early alpha
release, 0.4 in the middle of the week. After the whole 5 minutes of
celebration, the work resumed on the new features for the program. And fixing
typos in the documentation. A lot of typos. ;) But before the release, there
was some work done too:

* Updated the program's unit tests, especially related to the program's rules,
  to the new more verbose version of the tests.
* Updated the program's documentation with information about the `fix` type of
  rules.
* I stared work on the new rule to check if procedures have side effects. But
  during the work occurred that will need to add a Nim VM to the program to
  implement that kind of rule. I didn't want to add another big thing to the
  project just right before the next release, so I postponed the work on the
  rule for now. It will be added in the future versions of the program,
  especially that the VM will be needed for any rule which must check the whole
  project's code.
* Added option to *hasDoc* rule to enable checking for documentation also the
  fields of type's declarations.
* Added option to *paramsUsed* rule to enable checking for parameters usage in
  macros.
* As usual, the project's documentation updated with the information about the
  newest changes.
* And here the next release happened. ;) All changes below are in the
  repository version of the program.
* Started work on new type of setting for the project's configuration files:
  `reset`. As the name suggest, it allows resetting the program's configuration
  and have another settings set in the same file. It allows running several
  checks in the same execution of the program. An example: I merged settings
  for the program and the program's rules into the one file. There is still
  some work to do, but it should be done in the next week.
* The program's unit tests should now continue after encountering a bug. Here
  are also a couple of things to check before the work can be claimed as finished.

### [Wine cellar](https://www.laeran.pl/repositories/winecellar)

*A graphical user interface for managing Windows programs on FreeBSD*

That's a new thing here. It has for now a low priority in work, so please don't
expect too many things to report in the next weeks. As the description states,
it is a simple GUI for managing (installing, setting and removing). The work
just started here and everything is still in the organization mode. As usual,
the project is also mirrored on [GitHub](https://github.com/thindil/winecellar).
