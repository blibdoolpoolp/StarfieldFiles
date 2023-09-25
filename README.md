# Under Construction --- Check back soon!

# Blibdoolpoolp's Starfield Files (Fully GamePass & Steam Compatible)

## Overview

This is the spot I will keep my updated Starfield tweaks/mods files so I can share with my friends and anyone else who stumbles upon them. I aim to improve the quality of life, while also trying to keep the “cheatiness” to a minimum while maintaining immersion. My goal is to have everything as automated as possible so there is no need to manually type in any console commands and pull yourself out of the experience. 

This repo is going to have my StarfieldCustom.ini, as well as my combined.txt tweaks file, as well as any other tweak files needed for my setup. I will include everything here that I can for easy access to anyone who wants to play their game how I have mine setup. The actual mods that I have installed are the property of the original creators on Nexusmods.com, and as such I will just be providing links on where to find them,  and instructions on how to install them. 

NOTE: I am playing on the GamePass version, so none of these tweaks or mods are going to use the SFSE (Starfield Script Extender). I believe these tweaks and mods should all work for Steam as well, but many Steam mods will not work on the GamePass version if they use SFSE or other extensions incompatible with GamePass. A few of the tweaks I went into the SFSE plugin source files to discover the actual commands used, and translated them to be used for GamePass.


## READ/DO THIS FIRST BEFORE MODIFYING ANYTHING

The first thing anyone who wants to mod Starfield must do is run the Modfix by Crypton HERE (insert link). You must do this before you start installing mods or tweaks or anything you install could get ruined and you have to start all over. 

_Background on Why its Needed:_ When Starfield gets installed, for some reason it creates TWO “\Data\” folders, one in “My Documents\My Games\Starfield\”, and one in the install directory. These two Data folders conflict with each other and mess up any mods you try to install. The reason for this is that any in-game picture you take gets saved to a folder within the My Documents Data folder, and consequently, if there are any files within the that version of the Data folder, the game completely ignores the install directory Data folder, which is where the UI, Visual, Audio, etc. mods need to go.

This fix primarily creates a “directory junction” or “symlink” (effectively the same thing) between the Data folder inside the install directory and the one in the My Documents directory. Additionally, it changes the folder that in-game photos are saved to prevent them from breaking the mods (instead of saving them in the My Documents Data folder, they are saved in a new folder called Photos that is completely separate). This ensures that mods do not break, so it is crucially important.

## Important Files & Their Structure

StarfieldCustom.ini: This file is the one that you will insert into the folder listed below, it houses your “overrides” to the default Starfield.ini located inside the installation folder, as well as calls upon the combined.txt tweaks file to start each time the game is launched.

Located in: “C:\Users\<username>\My Documents\My Games\ Starfield\”

StarfieldPrefs.ini: This file is located in the same folder as StarfieldCustom.ini, so do NOT get them confused. In fact, do not touch this file at all unless you know what you’re doing, as this handles things like global display settings and such. 

Combined.txt: This file houses all the various tweaks we want loaded into the game before we load our save. All the commands in this file get sent to the console and executed in the Main Menu before the game is loaded. 
GamePass “Root” Directory Located in: “<GamePass Install Directory>\ Starfield\Content\”
Steam “Root” Directory Located in: “<Path to Steam>\Steam\steamapps\common\Starfield\”

NOTE: Since I have designed this for the GamePass version, I will be referring to the “...\Content\” folder a lot. This is the “root” directory for the GamePass install files, and is also the directory where the Starfield.exe is located. Steam users can follow this guide, and it will work, but your path is different, you have no “...\Content\” folder, everything is inside of the “…\Starfield\” folder itself as noted above.

Aside from that, everything should be equivalent. So just keep in mind, when I refer to the “…\Content\” folder, in Steam users’ case, I am talking about the “…\Starfield\” folder (as long as you’re in the folder where the Starfield.exe is, you’re good). 

This is very convenient and automated, but some commands are not effective until the game loads, and currently there is no way to have a pre-selected command file execute upon load. As such I am including a section on binding commands (and even whole batches of commands) to hotkeys so we never need to open the console manually if we don’t want to. 

NOTE: When adding mods and tweaks to your game, you will be using the GamePass "…\Starfield\Content\" folder as the root folder whenever a mod says extract into the root, this is where the Starfield.exe lives, and where many mods say to place them. This is different than the Steam version, which uses the "Starfield" folder as the root. THE ONLY TIME YOU WILL USE  THE "My Documents\My Games\Starfield\" FOLDER is when you first insert the StarfieldCustom.ini, and if you ever return to edit it. No mods should be installed here. 


## Important Files Function

### Starfield.ini, StarfieldCustom.ini, & StarfieldPrefs.ini

In both version of the game, Steam and GamePass, the file Starfield.ini should be created automatically in the install directory ( “Content\” or “Starfield\”, as discussed in the previous section) This contains (some) of the default values used to configure the game. The values within this file will always be on unless they are overridden, and affect how the game behaves by default. 

These default, “vanilla” values will be used UNLESS the same attribute is contained within the StarfieldCustom.ini (and contains a different value), or is altered in some way by one of our tweak commands. Anything that exists in the StarfieldCustom.ini overRIDES but doesn’t overWRITE the settings in Starfield.ini. This means it is easy to revert any changes made if wanted or needed, because as soon as that command line is removed from the StarfieldCustom.ini (or the entire file is removed), next time the game is started, those tweaked values are back to original. 

TO BE CLEAR: The default Starfield.ini will not be altered by using a StarfieldCustom.ini file, and you can (almost) always remove the file if you want to revert back to Vanilla settings and nothing bad will happen.

A WORD OF CAUTION: If you add new mods on top of my collection, there is a (low) chance that certain mods that get activated through the StarfieldCustom.ini file may permanently change your save. This involves the official Creation Kit not being released yet, and some involved mods dealing with .esp files have the potential to break your save. If you decide to add any mods to my collection, just be careful, read reviews first and make sure no game breaking bugs are present at the minimum.

HOWEVER, none of the tweaks or mods in my collection or this repo will permanently alter the game and can all be removed or reversed if wanted or needed, though I highly recommend taking backups of your saves, your StarfieldCustom.ini file, etc. before you make any significant changes.

StarfieldCustom.ini is NOT created automatically. I will provide both of the following, your choice…

1.	My personal StarfieldCustom.ini that has all of my tweaks incorporated into it, with comments above each command or group of commands explaining what they do. You can either use it as is or look it over and remove the tweaks you don't want.

        AND

2.	A mostly empty StarfieldCustom.ini template that has only been altered to enable modding, but no mods or tweaks applied.


### Root Folder & It’s Subfolders

Root Folder: As discussed previously, the “Root” folder of your game install directory is where you place most mods. I will explain now what types of mods go where inside of this directory. 

GamePass “Root” Directory Located in: “<GamePass Install Directory>\ Starfield\Content\”
Steam “Root” Directory Located in: “<Path to Steam>\Steam\steamapps\common\Starfield\”


Text (.txt) files: These files contain batch commands, the main one being “combined.txt” which houses the bulk of our commands in one convenient file. Additionally, if you have some other script/text files you want assigned to a hotkey, or if you only need to use it once or occasionally, not every startup of the game, you could place those in the root folder as well. These files should be placed in the root directory itself, with the Starfield.exe file. 

Directories - UI, Textures, Audio, etc.: Within the Data folder inside root, there are multiple other folders that correspond to different types of mods, including an Interface folder (UI mods), Textures for reskins of items, sounds for… sound replacements.. You get the idea. Usually though, the mod provides you with a Data folder inside of the mod’s zip folder that you just drag into the root folder, and it will automatically merge with the existing Data folder and put all of the contained files in the right place.

Directory – Hotkeys: This folder will be automatically created in the root folder, alongside Data and Starfield.exe, when you run the Starfield Hotkeys mod by registrator2000. This folder houses the Hotkeys.ini file which is where you can add keybinds for a large amount of in-game actions or console commands. Additionally, you can use it to create “Macros” (or aliases) for other console commands if you so desire. Such as “gimme=player.additem f 10000”, where every time you type gimme into the console, the player.additem f 10000 console command is used much more simply.

NOTE: The file that creates the Hotkeys folder and sets up the initial Hotkeys.ini file also creates a symlinked version of the Hotkeys folder into the “\My Documents\My Games\Starfield\” folder so the StarfieldCustom.ini can reference it, so do not be alarmed when you see the “second” folder, it’s just a symlinked copy.  

## FEATURES

This list is not exhaustive, as there are too many tweaks to fit, but this covers the most important and impactful ones. Some of the values within are vanilla values, but it allows you an easy, central location to change them if you would like.

### StarfieldCustom.ini

-	Enables Mod Support via “Loose Files” & \Photos dir: which basically means it allows the game to load in the various little files (mods) we put in the Data folder and it’s subfolders.
-	Jetpack Enhancement: Allows you to press and hold the jetpack button for as short or as long of a continuous stream as possible instead of being delivered in short bursts. Works in tandem with the JetpackOverhaul mod in the modlist below. 
-	Various Graphical Enhancements: that are designed to make the game look better while keeping the performance the same or better than vanilla.
-	Shortens Item-Grabbing Delay: 0.3 seconds for interactive objects, 0.15 for non. 
-	Increases Decal Count & Persistence: Allows more bullet hold decals to remain on bodies for longer periods of time, and be seen from farther away.
-	Enhances the Look of Space: Makes space darker, more realistic, immersive, and awe inspiring.
-	Performance Enhancements: Tweaks to behind the scenes settings that make the game run even smoother.
-	Streamlines the Main Menu: Removes the intro movies, message of the day, and eliminates the delay before loading your game. (Note: I would always wait at least a few seconds to make sure the Combined.txt script has time to run before you load.)
-	Fixes Alt-Tab: Have you ever Alt-Tabbed out of the game and it turned your PC into a laggy mess? This tweak keeps the game active in the background to prevent this lagginess upon switching windows via Alt-Tab (make sure to pause first or you might get killed by an enemy whilst distracted!) 
-	(Nearly) Eliminates Several Lengthy Animations: Makes the fade-in/out transitions much faster, including loading saves, fast travelling, and opening doors. 
-	



The part you have been waiting for

### Combined.txt (Tweaks)

### Root Folder

### Data & it's Subfolders

### Other Root Subfolders

## Where All Files Should Go







