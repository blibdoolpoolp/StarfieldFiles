
# Starfield `Hotkeys.ini` Configuration Guide

## Table of Contents
1. [Introduction](#introduction)
2. [Understanding `Hotkeys.ini`](#understanding-hotkeysini)
3. [My Personal Setup](#my-personal-setup)
4. [Power Management](#power-management)
5. [Additional Tips](#additional-tips)

## Introduction

Welcome to this README guide! This document aims to provide a comprehensive tutorial on how to customize your `Hotkeys.ini` file for the game Starfield. By tweaking this file, you can set up custom hotkeys and macros to enhance your in-game experience.

## Understanding `Hotkeys.ini`

### Macros: Creating Command Shortcuts

The `[Macros]` section in `Hotkeys.ini` is where you can define shortcuts for various console commands or sequences of commands. For instance, if you frequently use the command `player.getspaceship`, you can set up a macro like this:

`pgss=player.getspaceship`

Now, typing `pgss` in the game's console will execute the `player.getspaceship` command, making your gaming experience more streamlined.

### Hotkeys: Direct Action Buttons

The `[Hotkeys]` section allows you to map these macros—or even direct game commands—to specific keys on your keyboard. For example:

`F1=player.setav speedmult 130`

Pressing `F1` will execute the associated command, in this case, altering your character's speed.

## My Personal Setup

*Coming Soon: Examples of my personalized Macros and Hotkeys.*

## Power Management

### Dynamic Ship Referencing

Due to the fluctuating nature of Reference IDs in Bethesda's game engine, dynamic ship referencing can be challenging. Here are some strategies to manage this:

- **Session-based Reference ID**: Update the `pship` value every new gaming session if you're using non-named ships.
- **Named Reference ID**: Prefer using named ships like "Frontier" whose Reference IDs are stable.

### Power Management Script Breakdown

For those interested in managing spaceship power through hotkeys, each hotkey script has specific components. Here's a quick rundown:

- `if pgss != 0;`: Checks if you're in a spaceship. `pgss` is a macro for `player.getspaceship`.
- `prid pship1;`: Sets the Reference ID to `pship1`, a user-defined variable for your ship.
- `if gaps;`: Checks if there's a pilot in the ship's seat. `gaps` is shorthand for `getactorinshippilotseat != 0`.
- `bat ship1_power1;`: Executes a batch file to alter the ship's power settings.
- `endif;`: Closes the `if` statement.

## Additional Tips

Any `.txt` file with console commands can be activated in-game. Save the `.txt` file to the game's root directory. To activate, type `bat <filename WITHOUT .txt>` into the console.

For example, my `Hotkeys.ini` has `Alt-1` through `Alt-5` set up as power presets for my ships, ranging from weapon-focused configurations to gravity drive optimizations.

---

> For additional context or learning resources:
> - [Starfield Game Mechanics](https://www.google.com/search?q=Starfield+Game+Mechanics)
> - [Console Command Tutorials](https://www.google.com/search?q=Console+Command+Tutorials)
> - [INI File Documentation](https://www.google.com/search?q=INI+File+Documentation)
