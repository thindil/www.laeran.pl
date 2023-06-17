-- layout: default
-- title: Weekly development report 2023-06-17
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another week with nothing to report in the stable version. As usual, I suspect
I have blindness. :)

In the development version, as always, the best time for finding bugs is a
couple of days after a release. But there are some small changes too:

* Fixed bug with showing information about finishes stories in the knowledge
  screen.
* Fixed several typos in the game's documentation.
* Finished work on the list of modules in the player's ship's info screen. It
  now can be sorted by the additional info.
* Added ability to "remember" the amount of custom waiting time in the wait
  menu.
* As always, updated the game's documentation with information about the latest
  changes.
* The work to move the game into Nimland slowly moves forward. Around 15% of
  code are moved now, another small milestone reached. ;)
* And the old Ada code got some improvements.

### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

And the work on the next release slowly moves forward. This week brings some
new features to the program's configuration mostly:

* Finished work on new the program's configuration directive, `reset`,
  mentioned in the previous week. Looks like everything works as expected. ;)
* Updated the program's documentation with information about the new
  configuration's directive.
* The GitHub workflow updated to the new version of the program's configuration
  too.
* Added a couple of debug messages when parsing the program's configuration
  files.
* Added the new program's configuration directive, `message`. As its name
  suggest, it allows to print a message when the program is running. The first
  message is always show only once, but the subsequent, for example between
  rules settings, are show with every file checked.
* Same as above, the program's documentation was updated with information about
  how to use the new configuration directive.
* Added another configuration setting, `forcefixcommand`. If set to **1** or
  **true** it will force next rules to use the `fixcommand` setting for `fix`
  types of rules instead of their code related to the `fix` type of rules.
  It is also possible to disable this setting with set it to **0** or **false**
  in a configuration file.
* Should I mention that the project's documentation was updated with
  information about the new configuration option? :)
* The tool *gendoc* was updated to the new version of the program's
  configuration too.
* Fixed detection of documentation in objects' types declarations by *hasDoc*
  rule.
* **BREAKING:** *hasDoc* rule now require the option to set, which declarations
  should be checked for documentation. The old behavior is available by set
  option to `all` value, for example: `check hasDoc all`. Here are still some
  small changes which should be done in the next week.
* Started work on `fix` type of rule for *hasDoc* rule. At the moment only code
  for removing documentation is added, more work to come, of course in the next
  week. ;)

### [Wine cellar](https://www.laeran.pl/repositories/winecellar)

*A graphical user interface for managing Windows programs on FreeBSD*

As the project is on low priority, only one change this week: GitHub testing
workflow now tests the program on FreeBSD instead of Linux. After all, it is a
FreeBSD centric project. ;)

Speaking of which, happy 30th birthday FreeBSD. Let's hope for another 60 or more
years together. :)
