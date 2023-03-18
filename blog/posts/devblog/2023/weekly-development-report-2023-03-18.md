-- layout: default
-- title: Weekly development report 2023-03-18
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

The stable version again proved that I'm blind. Got one report of crash and
during investigating it I found more things to fix. At least, most of them are
not crashes. I will have some work in the next week here. For now, only bug
with showing empty types of items in the trade screen is fixed.

In the development version, I'm slowly reaching the halfway to the next big
release:

* Status of the module in the module's info dialog is now showed as a progress
  bar, instead of text only. "Moar" graphics. :)
* Added ability to set or remove the repair priority from the module in the
  module's info dialog.
* The change above also triggered other changes to the game. The new icon for
  the setting's button added with ability to set it in the game's themes.
* As usual, updated the game's modding documentation with information how to
  change the icon.
* Fixed crash during updating the player's ship cargo (especially in combat).
* Fixed crash when the player's ship crew member gains level in a skill.
* Fixed showing empty items types on the items types list in the trade screen.
* Again, some code moved from Ada to Nim.
* And the old Ada code got some cleanup too. As usual in almost the last two
  years. :)

And as mentioned above. Because the last development version of the game was
around four weeks ago, time for the new one. In around 24 hours since this
post, it will be available to download. With all new, fresh, unexpected
features. :)

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

Cleanup, refactoring but also a few new things adding week. As the project is
closing to the next release, it is time to start making the code a bit
civilized.

* Started using `varDeclared` rule on the nimalyzer itself. Of course, it found
  a lot of problems, which were fixed during the week.
* As the configuration files for the project and its rules are updated, the
  project's documentation was updated either.
* Added ability to set what kind of declarations should be checked if they have
  pragmas by `hasPragma` rule. It is generally breaking change. Now the rule's
  configuration requires one parameter, thus old configuration files will be
  invalid.
* The same ability added for `paramsUsed` rule. It is also breaking change.
* Updated the project's rules' documentation with information of the last
  changes to the rules.
* Fixed detection of documentation of templates. Now it should properly detect
  if a template has documentation or not.
* Fixed exit code of the program when *check* type of rules didn't check
  anything in a code.
* Started work on some code refactoring. For now, moved a couple of procedures
  to the new **utils** module and added tests for them.
