-- layout: default
-- title: Weekly development report 2023-05-06
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Again, nothing found in the stable version of the game in this week. I'm slowly
out of dad jokes about not finding bugs in my own code. ;)

The development version is still in the same place, just a bit closer to the
end of one work. :)

* Added ability to start enlarging the player's ship's hull from the module's
  info dialog.
* Added ability to assign crew members to the workshop in the module's info
  dialog, when it has set any crafting order.
* Redesigned a bit how information about the current working order is presented
  in the module's info dialog. It is needed for one thing, which will be added
  in the next week.
* Code conversion to Nim slowly moves forward. It results in less code, and
  probably more bugs. ;)
* And the old code got some cleanup. Like by the last, almost 750 days. :D


### [Nimalyzer](https://www.laeran.pl/repositories/nimalyzer)

*The static code analyzer for Nim programming language*

Back on trail with the work. The week started with some code cleanup and
styling and ended with started work on another big thing for the program:

* Added info about disabled test(s) to the project's tests. At the moment it
  is needed only for *localHides* rule.
* Finished rewriting some templates in **rules** module into macros. It now
  requires less pragmas around them, but looks more "cosmic" (unreadable). :)
* Updated *namedParams* rule, so it will not check `defined` procedure if it has
  the named parameter. The main reason is that adding a named parameter to it,
  causes error in the code.
* Updated *varDeclared* rule, so it will not check for type or value for
  declarations which are unpacking tuples. It is not necessary to check for the
  value, it is always supplied, and type declaration is not allowed here.
* Removed unnecessary `{.ruleOff.}` pragmas from the code.
* Better checking for rules configuration in a configuration file. Now it
  should be easier to add a new type of rules.
* Added ability to check for documentation for global public variables by
  *hasDoc* rule.
* Fixed checking for documentation of procedures, if any child has a
  documentation by *hasDoc* rules.
* Added missing code documentation.
* And updated the project's documentation about the last changes.
* Started work on the new type of rules: `fix`. At this moment the work is in
  early stage of development so, not too much to say or show. Generally, the
  rule's type will try either automatically fix any problems detected in the
  checked code, or more often, especially at the beginning, executing a command
  selected by the user, by default, opening the checked file in a text editor
  or IDE. Currently, only setting the command to execute for this kind of rule
  is added to the program. More things will probably arrive in the next week.
