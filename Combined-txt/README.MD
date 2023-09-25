# Installation of Combined.txt

1. Copy combined.txt into "Root" folder of Starfield.  
    * `GamePass “Root” Directory` Located in: “\<GamePass Install Directory>\Starfield\Content\”
    * `Steam “Root” Directory` Located in: “\<Path to Steam>\Steam\steamapps\common\Starfield\”
>[!IMPORTANT]  
>Make sure to verify that the "sStartingConsoleCommand=bat combined;" command (without quotes) is located in the StarfieldCustom.ini under [General]. This command is what makes this script run upon startup automatically.  

2. (Optional) Look through the tweaks and decide if you want to disable any, or AT YOUR OWN RISK edit any of the values. If you do want to disable any, add a ";" (semicolon, no quotes) at the very beginning of the line. This will comment it out and disable that command without erasing it, allowing you to re-enable it in the future if you wish, or if you only want to disable it temporarily. 


### If you ever want to add any more ".txt" (AKA bat) mods, do not append them to the StartingConsoleCommand line like this...  
> "sStartingConsoleCommand=bat combined; bat yourmod2; bat yourmod3;"  

### Instead, just open the combined.txt file, then copy-and-paste the contents of the other .txt/bat file directly into combined.txt. That's why it's called combined, it has many, many .txts all put together in one file, as many players have had issues trying to load multiple separate .txts/bats at once. 
    




