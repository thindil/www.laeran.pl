-- layout: blog
-- title: Weekly development report 2021-08-14
-- summary: Weekly development report from Bartek Jasicki various Open Source projects

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

Another quiet week in the stable version. The only change was the update to
the development documentation for the project, but nothing in the game itself.
I probably need help there to find something. :)

The development version work continues as usual. The mostly by adding sorting
options to various in-game lists:

* Work on updating the debug UI is finished. It should look better now. The
  last part, adding or removing in-game events, is done.
* The list of items in the trade screen can now be sorted by all columns. The
  work started in the last week is here finished too.
* Added option to sort the lists of modules in bases' shipyard. This took most
  of the week, but now should work.
* The list of recruits in bases also got sorting capabilities.
* Started work on adding ability to sort crafting recipes in craft screen.
  This is in a very early stage of development.
* Standard footer: still clearing the game's code and formatting it. Boring
  things. :)

### [TASHY2](https://www.laeran.pl/repositories/tashy2)

*Ada binding to Tcl/Tk, the new version of TASHY*

The package `Tk.TtkEntry` is finished for now. The whole code documentation is
on its place and all units tests (Which were updated too) work as expected.
After that, I updated a bit the demo program: it is now centered on the
screen, plus its "display" looks a bit better. And now, the work on binding for
Tk command **bind** started. While the binding isn't too complicated, it
requires adding also enumeration with all possible keysyms supported by the Tk
library. And this may take some time to add. Thus, the next week can be same
monotony like the last one. :)

### [Hunter](https://www.laeran.pl/repositories/hunter)

*Graphical File Manager for Linux (written in Ada)*

And finally, after around 10 months of work, the new, buggy, development
version of the program was released. That is something to celebrate... by
around 5 minutes. :) After that, back to the work:

* Updated the project documentation. Now it should be more obvious which
  libraries are needed to run the program. Let's hope it prevents some
  confusion. :)
* When confirming files and directories to delete, the program in both version
  now show only simple names, not the whole paths as previous. For example, it
  shows *test.txt* not */user/home/directory/test.txt*. I think it is more
  clear, but if someone prefer the old version, feel free to contact with me in
  that matter.
* Fixed one missing translation string in Polish language
* Fixed auto hiding questions "dialogs" in graphical version of the program.
  They really shouldn't auto hide. :)
* Standard, almost copy+pasted from the last weeks: some work with fixing
  problems reported by the AdaControl. Some things never changes. :)

### [YASS](https://www.laeran.pl/repositories/yass)

*Yet Another Static Site (generator) (written in Ada)*

Again and again and again: fixing the problems reported by AdaControl
continues. It is still at the `Pages` package. Also, fixed a new bug,
introduced in the last few days or weeks: editing the project's tags with the
program modules.

### [DockerAda](https://www.laeran.pl/repositories/dockerada)

*Various Docker images files related to the Ada programming language*

A new and not fully tested Docker image was added to the project: with Spark
2014 Discovery. It was also build thus it is available in the same place where
are other images.

### [Vim-Ada](https://github.com/thindil/vim-ada)

*Ready-to-deploy plugins and configuration which change Vim/NeoVim into (mostly
Ada) IDE*

And it is this time of the year again. Time for update the project. At this
moment only default configuration was updated with the new packages, removed a
few and updated default configuration for them:

* Package Vim-Header was removed. Its functionality is almost the same as
  package Snippets, thus in my opinion, not necessary here.
* Color theme Gruvbox was replaced by Gruvbox8. Which is smaller, faster and
  the most important, better works with various programming languages.
* Added two new packages: EasyMotion, for simpler movement inside the files and
  QuickUI for add some basic UI elements to the Vim/NeoVim. Also, `.vimrc` was
  updated with configuration for them.
