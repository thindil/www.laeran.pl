-- layout: default
-- title: Weekly development report 2022-12-31
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the last this year, the weekly development report or what was done in my
Open Source projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Again, but the last time in the year. :) Nothing to report in the stable version
of the game. All bugs probably wait to emerge in the next year.

The development version has to show something this week, even if the list is
short. One visible change is made to the game:

* Fixed several typos in changelog
* The most of the week spent on redesign of the map cell info window. Under the
  hood, it changed almost completely. This allowed to use more colors and fonts
  in the info. The new version looks [that](https://imgur.com/j6ZJ0Gr). Now I
  think if there are no too many colors ;), but usually, there will be less of
  them when presenting info about other map cells. We will see how it will
  work.
* Continue moving the code to Nim. Now the most of the code related to bases
  types is ported, just now I have to use it in the old code too.
* And of course, good, old code cleanup continues.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Another week of preparation for the next release of the shell. As I started
using it as my daily shell, some problems emerged from the code. The most of
them should be fixed now, but one or two are still on the table, or better in
the code ;)

* Finished redesigning the shell's unit tests to use them with `testament all`
  command. Now all the tests can be nicely merged into one. It boosted running
  them a bit.
* The work above required also updates to the tests' information about their
  outputs. It is now done either.
* Started work on cleaning the code's documentation. I checked how looks the
  generated documentation and decided to remove all headers from it. It took
  the most of the week, but there is still some work to do.
* Fixed setting the terminal title when the shell is in the batch mode. It was
  caused some problems, mostly by adding unnecessary things to the output of
  commands.
* Fixed shell hangs when input and output are broken. This fix is temporary
  which means it will perhaps work forever. :P Anyway, in rare occasions, when
  the shell can't access input and output it should now nicely close instead of
  hangs in an infinite loop.

### [Gameboost](https://www.laeran.pl/repositories/gameboost)

*Yet another simple shell script to tweak FreeBSD for gaming*

Similar to the Blues' script work in the previous week, only two changes:

* Added check if the user entered the proper password for the account
* Made the script more standardized with fixing the issues reported by the
  shellCheck.
