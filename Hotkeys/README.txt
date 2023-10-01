# Hotkeys.ini Readme

This README explains how to customize the Hotkeys.ini file for Starfield. This configuration file allows you to set custom hotkeys and macros for various in-game actions.

## How the Hotkeys.ini file Works  

The Hotkeys.ini file is divided into two main sections:  

#### Macros section

In the [Macros] section, you define custom aliases for longer or more complex game commands,  or sequences of commands. For example, if there's a command like player.getspaceship that you frequently use, you could create a macro like pgss=player.getspaceship. Now, whenever you type pgss in the game's console, it will perform the same action as player.getspaceship. This is incredibly useful for bundling together multiple commands or creating your own, easier-to-remember versions of existing commands.


#### Hotkeys: The Direct Action Buttons

Here you define the key-bindings for specific actions or macros. Now, let's say you don't even want to open the console to type pgss. You just want to press a single button and have it happen. That's where Hotkeys come in. In the [Hotkeys] section, you map these Macros—or even direct game commands—to specific keys on your keyboard.




## My Setup

### My Macros



## Power Management  

### Dynamic  Ship Referencing

The issue of dynamically referencing ships becomes significant due to the nature of Bethesda's game engine. Reference IDs can be unstable, particularly for non-named objects or characters. To mitigate this, you have two options:

Session-based Reference ID: Update the pship value for each new session if you're using non-named ships.
Named Reference ID: Stick to using named ships whose Reference IDs are less likely to change.

Note: I use the Frontier (heavily modified), which has a RefID that never changes. 

### Power Managment Setup

#### Breakdown of Components

if pgss != 0;: This checks if the player is in a spaceship. pgss is a macro for player.getspaceship, which returns the Reference ID of the spaceship the player is currently in.

prid pship1;: This sets the Reference ID to pship1. pship1 is a user-defined variable storing the Reference ID of a particular ship.

if gaps;: Checks if there's an actor in the pilot seat of the ship. gaps is a macro for getactorinshippilotseat != 0.

bat ship1_power1;: Executes a batch file named ship1_power1, which likely alters the power settings of the ship.

endif;: Closes the if statement.

else; echo "Player Not on Ship"; endif;: If the player is not in a ship, it prints "Player Not on Ship" to the console.

prid;: Resets the Reference ID. This is important to ensure that subsequent commands don't unintentionally manipulate the wrong object.

I have my configuration file setup so I can use hotkeys to manage my ship power. You will need to input the RefID to your ship in the "pship1" section, or if you have multiple ships, then you can list additional RefIDs in the pship2, pship3, or pship4 sections.  

Any .txt file that contains console commands can be activated in game. You must simply save the txt file to your root game install directory, and then in order to activate them in-game you must type "bat <name of .txt file WITHOUT .txt>" into the console. In my Hotkeys.ini, I have set up Alt-1 through Alt-5 as my power presets. Alt-1 activates shipX_power1, Alt-2 activates shipX_power2, etc. I have power1, power2, and power3, to provide full energy to the corresponding weapon, full power to shields, full power to engine, and any remaining power to the other weapons. Alt-4 is set up to provide full energy to the engine, the shields, and then remaining power to the weapons. Alt-5 is set up to provide full power to the grav drive, then remaining power to shields, then engine, then weapons. 



