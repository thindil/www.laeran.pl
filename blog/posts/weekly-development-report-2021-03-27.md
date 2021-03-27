-- layout: blog
-- title: Weekly development report 2021-03-27
-- filename: blog/posts/weekly-development-report-2021-03-27.html
-- author: Bartek Jasicki
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week. The most visible change this week was update Fossil
to the newest version. It brings some interesting options, for example a user
selectable themes for UI. The list of the project got short information about
every project. Now I just need to update the UI, so everything will work
properly. :) And back to the details about the projects.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And time for a few boring weekly reports. Yes, the whole development version
in the last year was focused only on one thing: the UI, but now as the next
major stable release incoming, the reports will be even more boring :) Anyway:

* I still was disappointed with the speed of loading the known bases list.
Also, finding anything on the list which has around one thousand entries is
a bit hard. Even navigating through that list was hard. Thus, I decided to
add pagination to it. It took some time to find an optimal approach to it
(as usual when something is done for the first time), but I think it was
worth. :) Now the whole list is blazing fast plus solves some other, more
technical problems related to it.
* The list of known events also got pagination.
* As I started testing more the game (read: playing it again) bugs start
emerged. A few of them were fixed in this week.
* As usual, a lot of work were done under the hood, mostly related to
clearing problems reported by the AdaControl static analysis tool.

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*


Finished fixing problems reported by AdaControl. The biggest problem
was that it reported all declared subprograms as unused. Thus, in every
package specification, rule `REDUCEABLE_SCOPE` for subprograms and variables is
disabled (only **use** scope is checked). The project unit tests were updated.
Some work on the project maintenance were done too: script to run AdaControl
check were fixed and the check itself was added to the standard test suite on
GitHub. The work on some code refactoring started. Current Tcl bindings should
be now a bit simpler and faster, the work moved to the Tk binding. Also added
some generic functions to easier get Tcl commands result in the proper Ada
type and another generic functions for evaluate Tcl code and get its result.
And the project documentation got update too, mainly related to the project's
test process and to the coding standards.

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

This time even a few new things arrived in the console version of the program:

* Added optional last modified info to the directory view.
* Started work on setting items permissions and default application. At this
  moment only the form is ready with ability to move inside it.
* Autofocus on preview window when setting info or preview for them.
* Fixed crash on pressing keys in empty directory view
* As usual, a lot of work with fixing problems reported by the AdaControl.

### [Bob](https://www.laeran.pl/repositories/bob)

*Non-Intelligent console assistant (written in Ada)*

Here also is finished work with AdaControl check. All looks good for now.
The check itself was added to the standard GitHub check. Added build script to
create release version of the program. Again, some small updates to the
project's documentation were done too.
