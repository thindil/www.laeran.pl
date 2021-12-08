-- layout: default
-- title: Weekly development report 2020-10-24
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../index.html
Welcome to the second development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://thindil.itch.io/steam-sky)

This time I break the tradition a little and add a few new screenshots here :)

The work on the new bases list is almost [done](https://imgur.com/d02nA3T).
There are still some small things to do, but the whole list should work now.
During the work there emerged problem with UI performance.

Because the bases list was used this same UI model as ship info lists, it was
obvious that there will be problems too. Thus, the ship info screen got also
some small changes. Also, as one of the players suggested, I've added some
space between each section in the ship info. [Here](https://imgur.com/ptbzLYV)
is the new look of the ship info screen.

Other things done this week: fixed some bugs related to the new UI, added some
new bugs as usual by some code cleanup and refactoring. :) And a bit more
seriously: adding the unit tests to continuous integration was a very good
idea, another crash prevented. :)

### [TASHY2](https://github.com/thindil/tashy2)

As the work on setup script finished at now, the work on binding finally
started. At this moment it is a very simple binding to Tcl: it is possible to
execute any Tcl command or code inside the Ada code and add new commands to
the Tcl from the Ada. Also, added unit tests to the binding and fixed the
continuous integration for the project. Plus started work on Tk binding.

### [Hunter](https://github.com/thindil/hunter)

Again week spent on fixing bugs in code and typos and grammars in the project
documentation. At least the code refactoring work was finished. Updating the
code documentation slowly going forward.

### [Bob](https://github.com/thindil/bob)

Announced the last week "more work" ended as updating the project documentation,
script to generate the code documentation and some other small changes to the
project organization. At this moment any part of the code wasn't touched yet.
