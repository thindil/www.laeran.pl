-- layout: default
-- title: Weekly development report 2022-06-04
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. As the new month started, the other project is going
to archive mode. This time it is Hunter. I think that for now it is the last
archived project. From now, I will focus only on two of them, thus there should
be more to report on them. At least when I will stop clearing their code. :)

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

This week, only a few typos found in the stable version of the game. And
probably a lot more to fix are around. :) Anyway, in around 24 hours since this
post a new, more grammar friendly and with a couple of other bugs fixed version
of the game will be available for download.

The development version going in its standard pace:

* The same typos, which fixed in the stable version, should be fixed in the
  development too.
* Updated in-game help with more detailed information how the maximum amount of
  items to buy or sale counted.
* Added information to the in-game logs about the difference between the base
  price and payment during trading. This difference is the effect of the
  player's reputation in the base and the Rhetoric skill of the crew member
  assigned to the Trader position.
* Information about maximum amount of items for sale or buy changed into a
  button, which fill the value with amount of items to trade.
* Also, added tooltips with information how the maximum amount counted to the
  trade dialog. All these changes should prevent confusion why sometimes the
  maximum amount of items for trade is different that it should be. :)
* Started work on better look text in the in-game help. For now, the help
  should be only better formatted, but some other changes are coming there too.
* This can be interesting for people who modify the game: I added an option
  to set color for special names and keyboard shortcuts in the help in the
  game's themes.
* Standard for the last month, the under-the-hood work with code cleanup
  slowly moves forward.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

Almost copy + paste from the previous week. The whole week spent on playing
with the code of the shell.

* Changed constant `EmptyString` to `emptyLimitedString` function. It should
  work better, especially should be thread safe.
* Removed the default value for *text* field in `initLimitedString` procedure.
  It caused also some changes in the code.
* Finished work on adding unit tests for `LimitedString` type. Now, every
  subprogram should have own test, some even tested in a few places. :) Also,
  all the tests are updated to the new version of the type.
* Fixed showing information about an error during Tab completion.
* Fixed showing an error information, sometimes they could go to the standard
  output instead of the standard error.
* Made a few types **distinct** which caused a lot of changes in the code. But
  at least, now it should be harder to make mistake with them. From the other
  side, I know myself too good to be sure that I still can do something wrong
  there. :P
* The change above triggered adding proper procedures to the types too. I think
  I will move each distinct type to separated modules, or it slowly ends as
  unreadable mess.
* All the changes in the code caused some problems with all unit tests. I'm
  slowly fixing them... and break with another changes. That was very
  interesting week. :)
* Also, started some work again on coding style: I'm trying to use `.type`
  notation anywhere it is possible. In my opinion, it looks better than braces
  notation especially if there are a few braces around.
