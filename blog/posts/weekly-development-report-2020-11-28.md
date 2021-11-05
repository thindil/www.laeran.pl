-- layout: blog
-- title: Weekly development report 2020-11-28
-- summary: Weekly development report from Bartek Jasicki various Open Source projects
Welcome to the weekly development report or what was done in my Open Source
projects in the last week.

### [Steam Sky](https://thindil.itch.io/steam-sky)

*Roguelike in a sky with steampunk theme (written in Ada)*

As they say: if you ask for troubles soon or later you will find any :) By the
last few weeks nobody was reported any bugs, so I decided to check for typos.
And in the stable version there is a real gold mine of them. I'm slowly fixing
them thus soon will be a new, more grammar friendly, stable release of the game
available. And because I'm a bit lazy (and my English is far from perfect) I
use for this tool called [LanguageTool](https://languagetool.org/).

In the development version, the standard three tasks were done this week:

* Fun with updating various dialogs is almost finished: most of them looks not
bad. There is still some work for later, but they now should look a lot better
than earlier. Also, some small general changes to UI like frame around last
messages window. The main game screen now looks [that](https://imgur.com/UduMwLm).
* Another week with changes to the game features or less PR version: fixing
the bugs :P Mainly related to the ship to ship combat UI.
* Fun with code refactoring and updating its documentation continues.

Plus the most important information: because the last development version was
released almost 4 weeks ago, thus now it is time for the new :) In less than
24 since this post a new development version will be available to download on
[GitHub](https://github.com/thindil/steamsky/releases) and [Itch.io](https://thindil.itch.io/steam-sky)

Also, something not related to the game development but to the game itself:
inspired by one player who was running Dwarf Fortress on iPhone via SSH, I've
tried to run Steam Sky on the Android phone via VNC protocol. Results are far
from perfect: a native version would be a lot better. It is playable just a
bit slow and definitely too small. You can see a short video [here](https://youtu.be/zNeKVdDtBPQ).
Now I need to find time to build an Android version of the game :)

### [TASHY2](https://github.com/thindil/tashy2)

*Ada binding to Tcl/Tk, based on TASHY*

* Added some unit tests for the bindings to C subprograms for manipulating Tcl
varibles. Also, the code related to them was moved to separated package
Tcl.Variables.
* Tk Button binding is finally finished: all commands and settings are
on their place, code documentation should be almost useful and added a few more
precondition checks to the various bindings. One breaking change there is that
Tk_Button type now is subtype of Tk_Widget instead a new type.
* Work on binding for Tk commands related to the grid geometry manager was
started: it is possible to add widgets to it, set grid anchor, get its bounding
box coordinates, configure or get configuration of the selected column and
started work on bindding for configuring a grid.

### [Hunter](https://github.com/thindil/hunter)

*Graphical File Manager for Linux (written in Ada)*

Generally, the whole week was dedicated to fixing bugs and updating the program
UI. Also, the Ada programming language syntax highlightning was updated with
aspects and pragmas. A few small changes under the hood with code refactoring
were done too.

### [tkBreeze](https://github.com/thindil/tkBreeze)

*Tk version of Breeze and Breeze Dark themes*

Here also only small changes: added option to move scrollbars with mouse wheel,
fixed some typos in README.md and removed unused code from the themes.
