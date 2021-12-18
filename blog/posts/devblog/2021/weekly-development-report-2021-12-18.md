-- layout: default
-- title: Weekly development report 2021-12-18
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version, nothing to report. Which mean, the work here is
probably finished. The development version soon enters its final preparation
state. But there is still one week to go. :)

In the development version, the quest for a better UI, and a few small
side-quests continue:

* Added tooltips to the map movement buttons.
* Replaced text on the player's ship movement buttons with icons. It looks now
  [that](https://imgur.com/FErUzT3).
* Fixed crash when trying to repair the player's ship in bases.
* Fixed crash when trying to heal wounded player's ship's crew members in bases.
* The move to button also has now changed look from text to icon.
* Fixed crash when trying to sell an item which is not available in a base.
* Added ability to maximize the selected information section in the ships'
  combat screen. [Here](https://i.imgur.com/N1uh0FI.mp4) is a short video how
  it works.
* Now it is always showing the player's ship status in the combat, not only
  when the ship damaged.
* As usual, a lot of changes invisible to players done in the game's code.
  There is a small chance that they don't introduce new bugs. :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The work on the project slowed a bit in this week. The main reason is at the
end of the post, a new project. ;) Anyway, some work done either. The first, I
replaced CVC4 theorem prover with Z3. As far I see it works at the same level as
the previous but Z3 is a lot faster than CVC4. It needs around 40-50% time less
to analyze the same code. And in the code itself: the whole week spent on
fixing various problems reported by Z3. :) Still around 30% of proofs await for
the fix, but it is slowly moving forward.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

The whole week spent on a few things:

* Continue work on adding translations to the options interface in the console
  version. The most of them should be translated or ready to translation now.
  But there is still some work to do.
* Updating the program's translations.
* Some code cleanup and refactors to made it simpler.
* Standard, copy+pasted from the last weeks: some work with fixing problems
  reported by the AdaControl. Some things never changes.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

That something completely different and new here. :) I found a new "toy" last
time and decided to give a try to it: [Nim](https://nim-lang.org) language. We
will see how it will go. At this moment is too early to have any opinions, but
for me, Nim looks very promising. Just it is even less popular than Ada. :) As
a test for the language I started a new project, [Nish](https://www.laeran.pl/repositories/nish).
It is as usual available also on [GitHub](https://github.com/thindil/nish) and
[GitLab](https://gitlab.com/thindil/nish). Currently, it is a very basic
command shell, tested only on Linux, but should work. Just may be a "bit"
insecure. :) I'm impressed how much done with so small amount of code. Also,
the Nim build system is very user-friendly.
