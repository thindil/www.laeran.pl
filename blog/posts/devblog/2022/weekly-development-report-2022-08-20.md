-- layout: default
-- title: Weekly development report 2022-08-20
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
-- backlink: ../../../index.html

Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://www.laeran.pl/repositories/steamsky)

*Roguelike in a sky with steampunk theme (written in Ada)*

And again the quiet week in the stable version, no one reported yet problems
with the newest stable version of the game. As usual, something is probably
missing. ;)

In the development version, work going in the normal pace. The list is a bit
shorter than usual, mostly because the first task took the most time of the
week.

* Started work on ability to select a few items in the player's ship's crew
  member's inventory. It also triggered some changes to how the checkboxes in
  the tables are presented. Selecting is now finished and in the next week I
  will work on using it, mostly to group wearing or taking off items.
* The change above required to add a new image for not checked checkboxes in
  the table.
* I updated my testing environment with some new packages which will be
  required in the future. Looks like everything works for now.
* Standard footer, at least it's slowly going to the end of the longest phase.
  The work on code cleanup and improvement of its readability continues.

### [Nish](https://www.laeran.pl/repositories/nish)

*The experimental command shell written in Nim*

This week brings some more visible changes to the shell. Mostly related to the
plugins system.

* Now all the code has added contracts. At this moment, they are very simple,
  but I hope, over time I will upgrade them.
* Updated the project documentation, mostly related to the shell's plugins'
  system and information about the coding standard used in the project.
* Switched the project's requirements to own version of NimContracts package. I
  have fixed a few bugs which are still present in the official version. Thanks
  to Nimble it shouldn't be an issue for the others.
* The plugins' system is under serious rework. It finally got versioning and
  the minimum version requirement for the plugins.
* The `info` API call updated to show the version of API used by the plugin and
  its supported API calls. That means the `info` call is now required for the
  plugins to work with the shell.
* Started work on redesign how the plugins are called by the shell. Earlier it
  was just call all enabled plugins all time. It could lead to very slow shell
  if many plugins are installed. Now it calls only the plugins which should be
  called and which are having support for the selected API calls. This work
  require some more time and tests to be finished.
* The test plugin updated to the new version of the shell's plugins' API.

### [Gameboost](https://www.laeran.pl/repositories/gameboost)

*Yet another simple shell script to tweak FreeBSD for gaming*

Here only one change this week. As per request, the script now detects the
values of kernel settings and some Nvidia card settings and restore them to
the previous values instead of some flat values.
