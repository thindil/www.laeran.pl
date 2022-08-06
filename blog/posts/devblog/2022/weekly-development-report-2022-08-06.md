-- layout: default
-- title: Weekly development report 2022-08-06
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Again, if someone looks deep enough, bugs will be found. During the play with
UI in the development version of the game, I found a couple of issues in the
stable version. Fortunately, nothing serious, they all are related to the
keyboard shortcut in various dialogs, so it can wait a week more, maybe I will
find others too. ;)

In the development version, as mentioned above, the work on better UI
continues:

* Added buttons to show mission on the map and start negotiating the mission
  to the mission info dialog.
* As everything is in one place, I removed the action menu from the available
  missions list in bases. Now, clicking on them just bring the more information
  dialog for the selected mission. Again, that should make UI navigation a
  little easier.
* Updated buttons in the accepting mission dialog in bases to show icons and
  texts like in the other dialogs.
* Fixed Tab traversing in the negotiating hiring recruit dialog and in the
  schools in bases.
* Fixed closing the negotiating hiring recruit and accepting the selected
  missions dialogs with Escape key.
* Started work on the better looking rename ship, crew members or ship's
  module dialog.
* As almost always, a lot of work done with code cleanup and generally making
  it more readable. Looks like this task is slowly going to the end. Very
  slowly. :)

And because the last development version of the game released 4 weeks ago,
now it is the time for another release. In around 24 hours since this post,
a new, shining as usual, development version of the game will be available
to download.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

And back on trail. After the previous week release now it is a time for some
code cleanup and refactoring tasks. As usual :)

* The main work in the week was adding contracts to the various subprograms in
  the shell. There is still some work to do, but I think I'm currently in the
  middle of the job.
* That change required also some updates to the project's unit tests.
* I've decided to use `nimble` for build, testing and generally managing the
  project. Thus, I removed old tasks for `nim` command and moved them to the
  nimble configuration. Also, the task for running the project's tests moved to
  the file.
* The last change triggered some changes to GitHub action too. It took a few
  tries to properly set everything but as far I see, everything works as
  expected.
* The project's documentation updated with information about the new commands
  to build or test the shell. In addition, the contributing guide updated with
  information about the coding standards used in the project. It probably will
  be again updated but after finishing the task with contracts.
* Updated also template for reporting bugs on GitHub.

### [Blues](https://www.laeran.pl/repositories/blues)

*The simple shell script to control Bluetooth sound devices on FreeBSD*

That something new here. As description says, it is a very simple project with
a couple of files, which arrived here. I've done it mostly as my backup for now.
In the future I wish to replace it with something more user-friendly. But at
this moment, enjoy the new project, available here and on [GitHub](https://github.com/thindil/blues). :)

