-- layout: blog
-- title: Weekly development report 2020-10-17
-- filename: blog/posts/weekly-development-report-2020-10-17.html
Welcome to the first and I hope not last development report or what was done in
my Open Source projects in the last week. At least this week was a bit
productive :)

### [Steam Sky](https://thindil.itch.io/steam-sky)

In the development version it is almost a new tradition, time for the week
with screenshots :) The most of the work was related to move the player's
ship's cargo to the ship info screen. Now it is a real command center - all
information about the ship (general, modules, crew and cargo) are on one
screen. Also, this screen allows to control each part of the player's ship. For
now, it looks good, just I'm curious how it will work with larger ships. To
compare with the current stable version, here is [the old ship info](https://imgur.com/h6RIms5)
and here is [the new](https://imgur.com/9dh1dEe). Additionally, the whole game
UI should be simpler with that - less keyboard shortcuts, shorter menu
options. Of course here is still some "small work" to do with the ship info,
something what I call "paper-cuts" - nothing big but may be a bit annoying on
longer play.

And another rework of the UI started too. This time the goal is to merge all
knowledge lists (like bases, events, missions, stories) into one screen too.
Also, as usual, some code refactoring and cleanup were done too. The next big
stable version will be very "revolutionary" (read: "full of bugs") :) At least
adding unit tests to continuous integration started paying back: only in this
week it prevented one regression bug in the code.

### [TASHY](https://github.com/thindil/tashy)

Work on this project at this moment is finished. All bindings are on their
place, the code documentation was updated too. And final (for the Tcl/Tk 8.6
version at least) release was done too. Now it is time on shift focus to...

### [TASHY2](https://github.com/thindil/tashy2)

This is continuation work of the project above. At this moment everything is
under organization and only a new setup script was created. The main reason of
existence of the project is that I want to clear and redesign the whole
binding. Also, I want to change license from old GNU GPLv2 with linking
exception to simple Apache 2.0. In the next week here should start arrive some
code.

### [Dockerada](https://github.com/thindil/dockerada)

Here work also finished for now. At least until the next release of Ubuntu.
Last changes here was setting exact version of Ubuntu to use and added
dist-upgrade command to Debian bases images.

### [Vim-ada](https://github.com/thindil/vim-ada)

The main included themes, PaperColor got some updates to Ada and Tcl syntax
highlighting. Also help for the project and vim-plug were updated same as
screenshots. And because the last release was almost one year ago the project got a
new release too in this week.

### [Hunter](https://github.com/thindil/hunter)

The most of the week was spent on fixing various bugs and the project
organization. Added Captain Obvious Manifesto or Code of Conduct also simple
script to run the debug version of the program. As usual, most work was done
under the hood: some updates to the code documentation and code refactoring.

### [Bob](https://github.com/thindil/bob)

Almost one year on hiatus the project is back on the table. At this
moment only the project version and Travis configuration were updated. More
work will come in the next week.
