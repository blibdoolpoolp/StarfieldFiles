# Blibdoolpoolp's Starfield Files
##  (Fully GamePass & Steam Compatible)
## Changelog


V0.5 - 9-25-2023 
  - Finished the folder structure for my StarfieldCustom.ini and combined.txt.  
                 - Created README.MDs for each of those files.  
                 - Added in the Hotkeys folder with my custom Hotkeys.ini file.  
                 - Wrote the main README.MD for the repo, including features of my CS.ini and combined.txt.  
                 - Added detailed informational sections about the file structure and functions of the main files we use for modding.  
                 - Started the Modlist section, got through the Critical section and made progress on the Essential & Great section.   

v0.1 - 9-24-2023 - Created the repo, designed outlines.
### To Do:

- [ ] Write the README for my custom Hotkeys

## Overview

This is the spot I will keep my updated Starfield tweaks/mods files so I can share with my friends and anyone else who stumbles upon them. I aim to improve the quality of life and add more fun, while also trying to keep the “cheatiness” to a minimum while maintaining immersion. My goal is to have everything as automated as possible so there is no need to manually type in any console commands and pull yourself out of the experience.

This repo is going to have my StarfieldCustom.ini, my  tweaks file, as well as any other tweak files needed for my setup. I will include everything here that I can for easy access to anyone who wants to play their game how I have mine setup. The actual mods that I have installed are the property of the original creators on Nexusmods.com, and as such I will just be providing links on where to find them,  and instructions on how to install them. 

NOTE: I am playing on the GamePass version, so none of these tweaks or mods are going to use the SFSE (Starfield Script Extender). I believe these tweaks and mods should all work for Steam as well, but many Steam mods will not work on the GamePass version if they use SFSE or other extensions incompatible with GamePass. A few of the tweaks I went into the SFSE plugin source files to discover the actual commands used, and translated them to be used for GamePass.

# FEATURES

This list is not exhaustive, as there are too many tweaks to fit, but this covers the most important and impactful ones. Some of the values within are vanilla values, but it allows you an easy, central location to change them if you would like.

 ## [StarfieldCustom.ini](StarfieldCustom-ini/StarfieldCustom.ini)


-	### **Enables Mod Support via:**
    * **Enabling “Loose Files”:** which basically means it allows the game to load in the various little files (mods) we put in the Data folder and it’s subfolders.  
    * **Changing Photos directory:** so taking in-game photos will not break your mods
-	### **Jetpack Enhancement:** 
    * Allows you to press and hold the jetpack button for as short or as long of a continuous stream as possible instead of being delivered in short bursts. Works in tandem with the JetpackOverhaul mod in the modlist below. 
-	### **Various Graphical Enhancements:** 
    * that are designed to make the game look better while keeping the performance the same or better than vanilla.
-	### **Shortened Item-Grabbing Delay:** 
    * 0.3 seconds for interactive objects, 0.15 for non. 
-	### **Increases Decal Count & Persistence:** 
    * Allows more bullet hold decals to remain on bodies for longer periods of time, and be seen from farther away.
-	### **Enhances the Look of Space:** 
    * Makes space darker, more realistic, immersive, and awe inspiring.
-	### **Performance Enhancements:** 
    * Tweaks to behind the scenes settings that make the game run even smoother.
-	### **Streamlines the Opening Sequence & Main Menu:** 
    * Removes the intro movies (necessary for mod support), the message of the day, and eliminates the delay before you  can interact with the menu and load your save. 
    *   >[!NOTE]   
        >Make sure to always wait at least a few seconds before loading your save to make sure the combined.txt script has time to run before you load.)
-	### **Fixed Alt-Tab:** 
    * Have you ever Alt-Tabbed out of the game and it turned your PC into a laggy mess? This tweak keeps the game active in the background to prevent this lagginess upon switching windows via Alt-Tab (make sure to pause first or you might get killed by an enemy whilst distracted!)  

-	### **(Nearly) Eliminates Several Lengthy Animations:** 
    * Makes the fade-in/out transitions much faster, including loading saves, fast travelling, and opening doors. 
-	### **And much more...**

## [Combined.txt](/Combined-txt/README.MD) (Tweaks) 
### Ship Stuff

* Increased zoom for landings on planets (not moons)
   * Easier to pick a specific spot on the planet for double/triple biomes
* Transfer inventory to ship from 2500 meters
* Dock with a station or another ship from 1500 meters

### Combat

* Forces all enemies to drop their armor set on death
* Increases reload speed slightly
* Increases spawn rate of legendary enemies

### General QOL Features

* Makes people get out of your way faster
* Makes lock-picking much easier but not brainless
* Increases player walk speed slightly so you can keep up with NPCs
* Food actually heals you a decent amount (still small, but up to 100HP)
* Food and chem buffs last 2x as long


### Planet Exploration

* Only need to scan 4 animals and 4 plants (of each species) for a full planet scan
* Increased scan distance
* Makes scanner scan the whole screen
* Makes you able to see resource veins from very far away


### Just for Fun / Just Cause

* Better notification messages on screen (first\-person, crude narration text)
* Makes NPCs blink more often during dialogue
* Makes much more bullet casings remain on the floor for immersion

### Experience & Leveling

* Increases XP for a range of small things to make them more worth doing
    * Cooking
    * Crafting
    * Exploring (eg. discovering new POIs)
    * Researching
    * Lock-picking
    * Speech challenges

### Vendors / Economy

* Makes vendors inventory and credits restock every 24 hours instead of 48
* Vendors pay more (Vanilla = 15% base, Tweak = 20%)
* Allows you to own 20 spaceships
* Cheaper to register stolen ships

# ↓↓↓ Modlist Located Below Detailed Installation Instructions ↓↓↓ 
    > [!IMPORTANT]
## ***!!!READ/DO THIS FIRST BEFORE MODIFYING ANYTHING!!!*** > [!IMPORTANT]
    > [!IMPORTANT]  
 
The first thing anyone who wants to mod Starfield must do is run the [Modfix by Crypton](https://www.nexusmods.com/starfield/mods/1367). You must do this before you start installing mods or tweaks or anything you install _will_ get ruined and you have to start all over.  
  
### _Background on Why it's Needed:_   
       When Starfield gets installed, for some reason it creates TWO “\Data\” folders, one in “My Documents\My Games\Starfield\”, and one in the install directory. These two Data folders conflict with each other and mess up any mods you try to install. The reason for this is that any in-game picture you take gets saved to a folder within the My Documents Data folder, and consequently, if there are any files within the that version of the Data folder, the game completely ignores the install directory Data folder, which is where the UI, Visual, Audio, etc. mods need to go.]

This fix primarily creates a “directory junction” or “symlink” (effectively the same thing) between the Data folder inside the install directory and the one in the My Documents directory. Additionally, it changes the folder that in-game photos are saved to prevent them from breaking the mods (instead of saving them in the My Documents Data folder, they are saved in a new folder called Photos that is completely separate). This ensures that mods do not break, so it is crucially important.


# Installation Process

The general, simplified process is this (more detail down below if this is troubling you):

1. Download and copy my StarfieldCustom.ini into My Documents\My Games\Starfield
2. Download and copy my combined.txt into game install directory (AKA root directory, shown below if you don't know)
3. Download and run the Modfix mod (top of the Modlist under "Critical Mod")
4. Install the mods you want from the modlist below, I recommend at least the Essential Mods, they're game changers.

## <u>Important File Structure & Function Information</u>

### __`NOTE: Depending on if you have the game through GamePass or Steam, your "root" game install directory will be different.`__

<u>GamePass “Root” Directory Located in:</u> __“\<GamePass Install Directory>\Starfield\Content\”__  
<u>Steam “Root” Directory Located in:</u> __“\<Steam Install Directory>\Steam\steamapps\common\Starfield\”__

Aside from that, everything should be equivalent. So just keep in mind, when I refer to the “…\Content\” folder, in Steam users’ case, I am talking about the “…\Starfield\” folder (as long as you’re in the folder where the Starfield.exe is, you’re good).

THE ONLY TIME YOU WILL USE the "My Documents\My Games\Starfield\" folder is when you first copy the StarfieldCustom.ini into it, or if you ever return to edit StarfieldCustom.ini. NO mods should be installed here, all of them should be put into the root game folder OR one of it's subfolders (such as Data) as indicated by the mod. 

### <u>File Structure</u>

**`StarfieldCustom.ini:`** This file is the one that you will insert into the "My Documents\My Games\Starfield\" folder, it contains your “overrides” to the default Starfield.ini located inside the installation folder, as well as calls upon the combined.txt tweaks file to start each time the game is launched.  

**`StarfieldPrefs.ini:`** This file is located in the same folder as StarfieldCustom.ini, so do NOT get them confused. In fact, **do not edit this at all** unless you really know what you’re doing, as this handles things like global display settings, controller settings, and such. It is automatically created by the game based on your in-game Options.   
↓↓↓  
**<u>StarfieldCustom.ini</u> & <u>StarfieldPrefs.ini</u> are BOTH Located in: <u>“C:\Users\<username>\My Documents\My Games\ Starfield\”</u>**

**`Combined.txt:`** This file houses all the various tweaks we want loaded into Starfield upon starting the game. All the commands in this file get sent to the console and executed in the Main Menu before your save is loaded. Combined.txt lives in the root game folder (where the .exe is).  
 

**`Starfield.ini:`** This is the master configuration file that is able to edit any setting in the game. **Do not edit this**, this should be kept vanilla in case you ever need to revert. This file is also located in the root game folder.  
↓↓↓  
**<u>Combined.txt</u> & <u>Starfield.ini</u> are BOTH located in: <u>your root game install directory.</u>** 

### <u>Function Information</u>

These files (StarfieldCustom.ini and combined.txt) make modding Starfield very convenient and automated, but some commands are not effective until the game loads, and currently there is no way to have a pre-selected command file execute after loading your game. As such I am including a section on binding commands (and even whole batches of commands) to hotkeys so we never need to open the console manually if we don’t want to. 

In both version of the game, Steam and GamePass, the file Starfield.ini should be created automatically in the root game install directory (“Content\” or “Starfield\”, as discussed in the previous section) This contains (some) of the default values used to configure the game. The values within this file will always be on unless they are overridden, and affect how the game behaves by default. 

These default, “vanilla” values will be used UNLESS the same attribute is contained within the StarfieldCustom.ini (and contains a different value), or is altered in some way by one of our tweak commands. Anything that exists in the StarfieldCustom.ini overRIDES but doesn’t overWRITE the settings in Starfield.ini. This means it is easy to revert any changes made if wanted or needed, because as soon as that command line is removed from the StarfieldCustom.ini (or the entire file is removed), next time the game is started, those tweaked values are back to original. 


## Important Files Function

### Starfield.ini, StarfieldCustom.ini, & StarfieldPrefs.ini



TO BE CLEAR: The default Starfield.ini will not be altered by using a StarfieldCustom.ini file, and you can (almost) always remove the file if you want to revert back to Vanilla settings and nothing bad will happen.

A WORD OF CAUTION: If you add new mods on top of my collection, there is a (low) chance that certain mods that get activated through the StarfieldCustom.ini file may permanently change your save. This involves the official Creation Kit not being released yet, and some involved mods dealing with .esp files have the potential to break your save. If you decide to add any mods to my collection, just be careful, read reviews first and make sure no game breaking bugs are present at the minimum.

HOWEVER, none of the tweaks or mods in my collection or this repo will permanently alter the game and can all be removed or reversed if wanted or needed, though I highly recommend taking backups of your saves, your StarfieldCustom.ini file, etc. before you make any significant changes.

StarfieldCustom.ini is NOT created automatically. I will provide both of the following, your choice…

1.	My personal StarfieldCustom.ini that has all of my tweaks incorporated into it, with comments above each command or group of commands explaining what they do. You can either use it as is or look it over and remove the tweaks you don't want.

     __AND__

2.	A mostly empty StarfieldCustom.ini template that has only been altered to enable modding, but no mods or tweaks applied.


### Root Folder & It’s Subfolders

Root Folder: As discussed previously, the “Root” folder of your game install directory is where you place most mods. I will explain now what types of mods go where inside of this directory. 

`GamePass “Root” Directory` Located in: “<GamePass Install Directory>\ Starfield\Content\”
`Steam “Root” Directory` Located in: “<Path to Steam>\Steam\steamapps\common\Starfield\”


Text (.txt) files: These files contain batch commands, the main one being “combined.txt” which houses the bulk of our commands in one convenient file. Additionally, if you have some other script/text files you want assigned to a hotkey (using the Starfield Hotkeys mod), or if you only need to use it once or occasionally, not every startup of the game, you could place those in the root folder as well. These files should be placed in the root directory itself, with the Starfield.exe file. 

Directories - UI, Textures, Audio, etc.: Within the Data folder inside root, there are multiple other folders that correspond to different types of mods, including an Interface folder (UI mods), Textures for reskins of items, sounds for… sound replacements.. You get the idea. Usually though, the mod provides you with a Data folder inside of the mod’s zip folder that you just drag into the root folder, and it will automatically merge with the existing Data folder and put all of the contained files in the right place.

Directory – Hotkeys: This folder will be automatically created in the root folder, alongside Data and Starfield.exe, when you run the Starfield Hotkeys mod by registrator2000. This folder houses the Hotkeys.ini file which is where you can add keybinds for a large amount of in-game actions or console commands. Additionally, you can use it to create “Macros” (or aliases) for other console commands if you so desire. Such as “gimme=player.additem f 10000”, where every time you type gimme into the console, the player.additem f 10000 console command is used much more simply.

NOTE: The file that creates the Hotkeys folder and sets up the initial Hotkeys.ini file also creates a symlinked version of the Hotkeys folder into the “\My Documents\My Games\Starfield\” folder so the StarfieldCustom.ini can reference it, so do not be alarmed when you see the “second” folder, it’s just a symlinked copy.  

# Modlist

## Critical Mod(s) - you MUST have the Modfix for the tweaks & any other mod to work, and the Achievement Enabler to not disable achievements from using the other tweaks/mods (if you care about that)

* [Modfix by Crypton](https://www.nexusmods.com/starfield/mods/1367) - Needed for mods to work correctly and not break. 
    * `Installation` Download the .cmd file, place it into your ROOT directory (with Starfield.exe) and run it. It should be able to automagically find everything it needs at this point, but if it can't find the install folder you will have to manually specify it (that is why we place it into the root directory first).
    
*  **One of the Achievement Enablers**
    * **GamePass users:** Install the [Achievement Enabler by Priqrade](https://www.nexusmods.com/starfield/mods/252) - This mod does exactly what it says, enables achievements even while you are using mods. 
        * `Installation` Create a folder in the root game install folder called Plugins if you don't have it. Download the .asi file from the Nexus link. Place it into the Plugins folder. Then, follow [this link](https://github.com/ThirteenAG/Ultimate-ASI-Loader) and download their copy of "bink2w64.dll". Rename the <i>real</i> "bink2w64.dll" from your root game install folder to "bink2w64Hooked.dll", and then paste in the new "bink2w64.dll" you just downloaded into the same folder. In the end, you will have one file named "bink2w64Hooked.dll", the original .dll that has been renamed, and "bink2w64.dll", the new .dll that loads the .asi file we placed into plugins. All should work great now. (If you don't have "bink2w64.dll", then follow the instructions on the mod page for dinput8.dll, but I have not heard of a single person mentioning they had that file.
   * **Steam users:** Install either the one above (it works with Steam, but Steam's version doesn't work with GamePass) or [Baka Achievement Enabler](https://www.nexusmods.com/starfield/mods/658). For this one you will need SFSE which is only available for the Steam version so I cannot help you there.
        * `Installation` Download SFSE according to the instructions on the Mod page and then use it. 
        
## Essential Mods - Ones that I cannot _imagine_ playing without

* [Starfield Hotkeys by registrator2000](https://www.nexusmods.com/starfield/mods/1578) - This mod extends the functionality of console commands massively, allowing you to assign in-game functions and/or console commands to keyboard buttons, as well as write "Macros" (AKA aliases) for commands. I am going to include my Hotkeys.ini file which includes hotkeys for managing your ship power, setting your movement speed to 400% for when you need to run 2,000 meters to the nearest POI and a corresponding hotkey for setting it back to normal once you are close. The possibilities are endless. 
    * `Installation` Download the files, and run the enable_hotkeys.cmd. This adds the needed lines to StarfieldCustom.ini if they aren't there, creates a symlinked Hotkeys folder in both the My Documents - Starfield directory (so StarfieldCustom.ini can access it) and your game install folder, and copies the Hotkeys.ini file into that new folder. You can configure your hotkeys directly in the ini file (my preferred option), or you can do it directly through the in-game console.
    * [See my Hotkeys folder for my custom built hotkeys](/Hotkeys), credit to [Braneth](https://www.nexusmods.com/users/37941390) and [stavanzer](https://www.nexusmods.com/users/7341897) for coming up with the general format for the ship power hotkeys that I tweaked. Read the README within my Hotkeys folder for a rundown. 

* [StarUI Inventory by m8r98a4f2](https://www.nexusmods.com/starfield/mods/773) - This mod completely overhauls the shitty vanilla inventory system. It gives you so much more information about your items in a convenient, spreadsheet (yet stylish) type display. It features custom subcategories for each major category the game gives you, such as allowing you to go into your AID category and further refine it into Meds, Chems, Food, etc. Fully customizable via ini, I like to add on Value/Mass, Value/Stack and Mass/Stack so I can really get into the details of my inventory. 
    * `Installation` Download the latest version and open the .zip. Open the Data folder inside of the root directory, and drag and drop the "Interface" folder into it. 
    
* [Jetpack Overhaul by IxionXVII](https://www.nexusmods.com/starfield/mods/569) - This mod makes your jetpack MUCH more like, well, a jetpack. You can choose to do short bursts, burn your entire meter out in one long, sustained blast, or anywhere in between. It's one of those things that I'm so used to, it doesn't seem like a "big deal", but imagining the game only being able to do those anooying bursts you can't control the length of sounds horrible. The game should have released this way.
    * `Installation` Thus far, this is the only mod that requires you to use the console to enable it (but only one time). This is due to these commands only needing to be used once and then working forever on your save. The mod download also comes with a "JetpackVanilla.txt" to be entered into the console to uninstall it (though once you install it, you ain't going back, trust me!) 
    
    * If you're using my StarfieldCustom.ini, it already has the lines needed, so go ahead and move onto the next step. If you are using a different StarfieldCustom.ini, then you're doing to need to add: 
    `[Boostpack]``
    `bUsePressAndHoldControls=1`
    
    * To enable it, you simply download the mod folder, copy-and-paste the "JetpackOverhaul.txt" into your root game install folder (same folder as combined.txt, they're both the same type of bat file, however we want combined.txt to run every time we start the game so we include it in the StarfieldCustom.ini, whereas this one just needs to be run once manually). Load into your game and press the ~ button to pull up the console. Then type in "bat JetpackOverhaul" and hit enter (no quotes). The bat will do it's thing and you're good. 
    
* [Smooth Ship Reticle (NOT FULL UI OVERHAUL) by alexbulluk](https://www.nexusmods.com/starfield/mods/270) - This mod takes the super choppy vanila starship reticle and makes it smooth as butter. The Full UI overhaul is not compatible with StarUI, and StarUI makes the inventory smooth already, but it doesn't touch the starship reticle/HUD. 


## Great Mods - Personal preference if you want to use them or not, they don't make or break the game but they do enhance the experience

* [Scanner Boost by oogabooga66](https://www.nexusmods.com/starfield/mods/829) - I already have increased the scanner range in my combined.txt file to 60m, but this mod implements it even better I believe in certain ways. There are multiple variants, where they not only boost your base range, but also increase the range of the Scanner upgrades, making it much more worthwhile to put points into Scanning. They have a balanced Variant which only increases the base range by an extra 10m (to 20m base), and each upgrade gives you 5m more than the vanilla upgrades (15m per level), and also a much more generous version starting at 100m and increasing by 25m per level. Pick your poison, or just use what I already have in my combined.txt file. I'm too used to the 60m to go back down to 20m, but I feel 100m is too much for me, so I'm torn. I guess this gives you three options!
    * `Installation` Go with my presets already included in combined.txt, or download the version of your choice, and all you need to do is open the Scan.txt file and paste the lines into your combined.txt (ignore the StarfieldCustom.ini included with the mod). If you're using my combined.txt then you should find the section where I adjust the scanner settings and paste your desired settings over them (located under the [Exploration] tag).
    
    
# Changelog


V0.5 - 9-25-2023 - Finished the folder structure for my StarfieldCustom.ini and combined.txt.
                 - Created README.MDs for each of those files.
                 - Added in the Hotkeys folder with my custom Hotkeys.ini file.
                 - Wrote the main README.MD for the repo, including features of my CS.ini and combined.txt.
                 - Added detailed informational sections about the file structure and functions of the main files we use for modding.
                 - Started the Modlist section, got through the Critical section and made progress on the Essential & Great section. 

v0.1 - 9-24-2023 - Created the repo, designed outlines.









