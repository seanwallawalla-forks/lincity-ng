
***

![LinCity_NG.png](LinCity_NG.png)

# LinCity-NG

_a city simulation game_

[https://github.com/lincity-ng/lincity-ng](https://github.com/lincity-ng/lincity-ng)

Contents:

[1. Introduction](#1-Introduction)

[2. Building and Installation](#2-Building-and-Installation)

[3. Gameplay](#3-Gameplay)

[4. Contact](#4-Contact)

<!-- ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ !-->

## 1 Introduction
LinCity-NG is a city simulation game. It is a polished and improved
version of the classic LinCity game. In the game, you are required
to build and maintain a city. You can win the game either by
building a sustainable economy or by evacuating all citizens with
spaceships.



<!-- ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ !-->

## 2 Building and Installation


These are generic instructions, please see the wiki for more specific instructions

2.1 Prerequisites

The game depends on some tools and libraries to be present, before
you can start building it. Here's a list of them:

* normal gnu compiler and additional tools (g++ version 3.2 or later is
  required at the moment)

* perforce jam 2.5 or later (used as build tool)
  ftp://ftp.perforce.com/pub/jam

* SDL 1.2.5 or later
  http://www.libsdl.org

* SDL_mixer 1.2.4 or later (with ogg-support enabled)
  http://www.libsdl.org/projects/SDL_mixer/

* SDL_image 1.2.3 or later (with png support)
  http://www.libsdl.org/projects/SDL_image/

* SDL_ttf 2.0.8 or later
  http://www.libsdl.org/projects/SDL_ttf/

* SDL_gfx 2.0.13 or later
  http://www.ferzkopp.net/~aschiffler/Software/SDL_gfx-2.0

* PhysicsFS 1.0.0 or later (use stable, NOT development branch 1.1.0)
  http://www.icculus.org/physfs/

* zlib 1.0 or later
  http://www.gzip.org/zlib/

* libxml 2.6.11 or later
  http://xmlsoft.org/

If you use packages from you distribution pay attention that you need
the header files in addition to the libraries. They are often in 
separate *-dev packages. Eg. for physfs you need libphysfs and libphysfs-dev.

2.2 Building

To build and install the game use the following commands:

    ./configure 
    jam

If you want to install the game, run as root:
    jam install

(If you compile the svn version you have to run ./autogen.sh first.)

The configure script also lets you set some more options like the installation
directory (--prefix argument). You'll get a full list of these if you invoke
"configure --help".

2.3 Starting the game

You can start the game by typing

    lincity-ng

2.4 Exit the game

If you are in the main menu, you can quit the program also by
pressing 'ESCAPE' or '^c'. This might be a way to terminate the
program even if the selected video-mode is not working as expected.

<!-- ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ !-->

## 3 Gameplay

See the ingame help [F1] for more details.


3.1 Objective

You can win Lincity either by building a sustainable economy or
by evacuating all citizens with spaceships.

3.2 Controls

Mouse

any:
 Click on Minimap shows the selected Area on mainscreen.

right:
 Drag mainscreen with right mousebutton.
 right click on mainscreen centers to tile under cursor.
 select tool from menu root
 show help on tool

middle:
 middle click on mainscreen to show information about area under cursor.

left:
 Perform action depending on selected tool. Bulldoze, show Information,
 construct building.
 open Tool-Selection-Menus 
 select tool from menus

wheel:
 up: zoom in
 down: zoom out

Keyboard

 ESCAPE switch to query tool

 KP_PLUS: zoom in
 KP_MINUS zoom out
 KP_ENTER zoom 100%

 KP5 put middle of the map in the center of the main screen  

 KP9 scroll main screen north
 KP1 scroll main screen south
 KP7 scroll main screen west
 KP3 scroll main screen east

 KP2 scroll main screen se 
 KP4 scroll main screen sw 
 KP6 scroll main screen se 
 KP8 scroll main screen nw 
 same with cursor

use shift + direction to scroll faster

 h  to hide high buildings. Press h again to show them.
 v  to cycle through MiniMap-overlay modes
 b  toggle between current tool and bulldoze mode 
 F1 Help
 
 F12 quick save
 F9  quick load

<!-- ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ !-->

## 4 Contact

Bugs should be reported to:
    https://github.com/lincity-ng/lincity-ng/issues
    
You can contact us at the lincity-ng-devel mailinglist:
    http://lists.fedorahosted.org/mailman/listinfo/lincity-ng-devel
or you might be able to catch us in irc at irc.freenode.net #lincity.

Visit our homepage: https://github.com/lincity-ng/lincity-ng

***
