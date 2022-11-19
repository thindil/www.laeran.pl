-- layout: default
-- title: Weekly development report 2022-11-19
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

In the stable version, I think I found enough bugs for the new release. As far
I know the life, I will find another on Monday. :) Anyway, in around 24 hours
since this post, a new stable version of the game will be available for
download.

The development version has less visible changes this week, but a lot under
the hood.

* Fixed setting the list of available items' types during trading, looting and
  in the player's ship's cargo. It wasn't showing the items' types if the items
  were on later pages of the list.
* Fixed keyboard shortcuts for changing the player's ship's speed. This and
  above are fixed in the stable version too.
* I continued updating the knowledge's screen. To make it more colorful, I
  added a separated color on the lists, for a base or an event, which are
  currently set as the destination for the player's ship. The same feature for
  the missions' list will be added soon.
* Again, some code moved to Nim. I hope it doesn't generate too many new bugs.
  :) Generally, Nim code grows slowly, but also reduces the total size of the
  game's code.
* In the old code, as usual, cleanup, refactoring and other boring things. :)

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

The cleanup week again. This time the work was related mostly to the project's
tests, but at the end there were also some experiments with the shell itself.


* The input code are moved to the separated procedures to share between normal
  user's input and the forms' input.
* All the new code has its own tests added too.
* The most of the week spent on adding fail's messages to the tests assertions.
  Now when the test fail it should produce a more understandable result.
* Updated the project dependencies to use the official version of the Contracts
  package again. The author merged my changes some time ago plus added a couple
  of own. Worth to use it. :)
* Updated the project's documentation with information about its dependencies.
* As the shell is "experimental" time for the first failed experiment. :) I was
  thinking about splitting the output and input to separated fields. After
  around two days of trying it, I decided that it isn't good idea: the first,
  it doesn't bring any advantages and can only cause confusion, the second,
  implementing it could require a lot of work and bring the same amount of
  bugs. The third, I think here are a few more interesting options to add to
  the shell. So after some changes in the code I reverted them to the old state
  and moved to work on different things. It seems like the shell at end will
  not be that "experimental" as I though. :)
