# phen6mv5
Updated version of a WAW trickshotting mod currently being worked on.

----------------------------------------------------------------------------------------------
CFG FUNCTION CALLING - things such as save, load, and even killcam skip can be enabled via cfg.
They don't work like IW4X unfortunately, but they work nevertheless. The format is as follows..
EXAMPLE - Get Coords function in your CFG file should look like this..
---------------------------------------------------------------------------------------------------------------------------------------------
set getmycords(or whatever the fuck you wanna call it) "getcords 1" - getcords 1 is what the function listens for, so this cannot be changed.
---------------------------------------------------------------------------------------------------------------------------------------------
Currently only have the following functions set up.
getcords 1 - Print your current coords on screen - posx, posy, posz & viewpoint. The 0's on both sides of the viewpoint are not needed.
loadcords 1 - Loads your saved cords and saves it as your spawn/load position.
kcskip 1 - As long as you use this within 4 seconds after the round ends, it will skip the killcam. Usefull if you've fucked up.
ebtoggle 1 - Turns on EB everywhere.
bombmala 1 - Pulls out a bomb mala.

KILLCAM SKIP // BINDS AND GLITCHES MENU - Two versions are available here, the cfg version just skips the killcam to save time.
The menu version however also shortens the intermission screen, so that a cleaner respawn shot can be done.
Not entirely sure what the time has been set to and I can't be bothered looking. I think it's between 2 - 3 seconds after the kill.
The killcam will only skip for one round and it will be back to normal on the next one.

BROKEN SCOPE // BINDS AND GLITCHES MENU - Something funky I found while poking around. I'm not sure if it has a proper name, so it's called Broken scope in the menu or B-scope.
This removes your sniper scope hud, while still retaining the zoom and some of the FOV. Looks like closed curtains. CFG for this will be added when I wrap my head around a proper toggle.

EZ MALA // BINDS AND GLITCHES MENU - Old faithful. Pull equipment do mala, simple. +smoke malas are currently kinda bugged and revert to a +frag mala on usage. I will figure it out sooner or later, leaving as is for now.
I had planned on adding perk equipments to this list but they function as full on weapons unfortunately so they are proving difficult. I will look into it, sometime in the future.

CORDS FORMAT IN CFG - This is how your cords should be formatted in your cfg folder in order to load them in as needed.
-----------------------------------------------------------------------------------
set cords "posx 771.125;posy 818.847;posz 272.125;view -138.046;wait 5;loadcords 1"
-----------------------------------------------------------------------------------
This will save your cords as a dvar and execute them. If you have already saved your cords in game, change them in your CFG file and execute them again.

ALWAYS CANS // TRICKSHOT MENU - What it says on the tin, always can your weapon on pullout. Can change this to only can certain weapons if needed but I don't think it'll be needed on this game.

MOST IMPORTANT - When your naming shit in your CFG folder, make sure you don't
name your vstr the same name as the function (or dvar is this case) that you are trying to call/change.
EXAMPLE - Do not name the getcords func like this..
-------------------------------------------------------------------------------------------------------------------------------------------------------------
set getcords "getcords 1" - Doing so will make the menu take a giant shit and it will throw you an erorr about an unknown function 0, or something of the sort.
-------------------------------------------------------------------------------------------------------------------------------------------------------------

CFG EB - Slot "ebtoggle 1" into your script before your killshot and it'll do it's thing. Lasts
for one "+attack" so if for some reason it doesn't work maybe put it earlier in the script.
This won't carry over between rounds, so enable it when needed.

DROP WEAPON // WEAPON MENU - Drops the weapon you are currently holding on the ground.

HARDCORE UI HUD TOGGLE - Toggle between normal UI and hardcore UI. Mainly added this for my own benefit to see what's going on during testing but it's here if you need it.

SMALL THINGS
- Controls have been frozen while in the menu, so you don't have to listen to 900 rounds going off as you navigate the menu.
- Coords have been removed on spawn, so they aren't visible if you are doing a respawn shot.
- Bot names can be added/changed via bots.txt file provided.

PLANNED FEATURES
- Mala fixes - +stuns currently pull and default back to frags, hopefully perk equipment like satchels and bettys can be added also.
- More CFG options/ functions - Don't know much about this game and what's possible. Also the format for CFG and available native functions
  are alot different to 4X, so I'll be learning as I go. If you want features added ask, because I likely don't even know they exist.
- Alt swaps - Currently available in the menu sort of, but I'm planning to add Alt swaps that stick during round switches and class swaps.
- Equipment cancels - +frag and +smoke putaways after a weapnext/weapprev.
- Instashoots - ...... Shoot instantly????
- Velo/bolt - Never used these or implemented them, will look into this.
