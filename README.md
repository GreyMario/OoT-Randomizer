# OoT-Randomizer

This program is a randomizer for the Nintendo 64 version of _The Legend of Zelda: Ocarina of Time_.

# Installation

The current Windows release build is version 2.0, [available here](https://github.com/AmazingAmpharos/OoT-Randomizer/releases/tag/v2.0). Simply download and run the linked installer.

If you do not have Windows or you want to run from the Python source, [clone or download the repository (or one of its forks)](https://github.com/AmazingAmpharos/OoT-Randomizer) or [download the source code for the release](https://github.com/AmazingAmpharos/OoT-Randomizer/releases/tag/v2.0). Install [Python 3.6](https://www.python.org/) or better, then run `Gui.py` for a user interface or `OoTRandomizer.py` for a command-line interface.

You will need to acquire a copy of the _United States 1.0_ version of _The Legend of Zelda: Ocarina of Time_ to use with this program. It must be the United States v1.0 release; no other release is compatible with this program.

You will also likely need an _emulator_ in order to run the randomized output.
- RetroArch is our top recommendation for stability and accuracy.
- BizHawk is acceptable, but there is a known issue with the fishing minigame.  
  If you find yourself unable to hook and reel in a fish, save your game and perform a hard reset to fix the issue.
- Please do not use Project64 to run the randomized ROM.  
  Project64 has been demonstrated to be an inaccurate and unstable emulator. No technical support will be provided for an issue that occurs while using Project64, unless it can be proven to occur in an accurate emulator or on real N64 hardware.

The randomized output may also be injected into a Wii Virtual Console channel or used on an Everdrive to play on the real Nintendo 64 hardware. Both are beyond the scope of this readme.

## Please Note: On Stability and Crashing (no, really, this is important.)

This program offers the option to `Compress patched ROM` at seed generation. **Always use this option.** This eliminates major stability issues when using an emulator to play, the most notable of which is **crashing when pausing or dying.**

This option was originally provided as a courtesy to Everdrive users, as the original Nintendo 64 hardware does not crash when using an uncompressed output. It has since been demonstrated that the compressed output works just as well, if not better. Included with the program is a compression utility tailor-made for _Ocarina of Time_.

# General Description

This program is a tool which takes _The Legend of Zelda: Ocarina of Time_ as an input and outputs a modified, "randomized" version for a more dynamic play experience which tests your knowledge of the game's mechanics. The randomization process uses proper "logic" to ensure that every generated seed will always be completable without the use of glitches, and the logic accounts for the worst order a player can possibly use keys in to prevent softlocks.

As of the 2.0 release, the following rules apply to the randomization:

### Global Item Pool
The items and locations in the **Global Item Pool** include the following locations and their vanilla contents:
- All items found within chests, _including_ all chests found within grottos across Hyrule.
  - The exception is the chests within the Treasure Minigame in Castle Town _leading up to_ the grand prize chest.  
   The grand prize itself (a Piece of Heart in the original game) is shuffled.
  - Dungeon items (Maps, Compasses, Small Keys, and Boss Keys) will only appear in the dungeon they belong to.  
   They may still be shuffled among the chests within their parent dungeon and may even appear on the boss.
- All Heart Containers
- The unique prizes from all minigames (the prizes you may only win once)
- The three Business Scrubs that sell unique one-time upgrades
- All freestanding Pieces of Heart, including those created by minigames (Dampe's Gravedigging, Goron City Spinning Pot)
- All gifts from Great Fairy Fountains
- Fire Arrows and Ruto's Letter
- All other sidequests, most notably:
  - The prizes for turning in 10, 20, 30, 40, and 50 Gold Skulltula Tokens
  - The prizes for Skull Mask and Mask of Truth in the Theater grotto in Lost Woods
  - Anju's Pocket Egg
    - Anju will give you a random item as an adult instead of the Pocket Egg.
    - You will find _one_ randomly selected Adult Trading Quest item (never the Odd Potion) in the global item pool.  
      Complete the Adult Trading Quest as normal starting from the randomly selected item once you find it.
  - The reward Biggoron gives you for turning in the Claim Check
    - The real Biggoron Sword may appear anywhere in the global item pool.
  - Turning in 10 Big Poes
 
### Song Pool
Songs are shuffled among their own locations. For example, Malon may teach you the Minuet of Forest and Guru-Guru may tell you the song that drove him mad was the Song of Time. Songs will only ever appear at song locations. You will never receive an item at a song location, or a song from the global item pool.

### Medallions, Spiritual Stones, and Link's Pocket
The eight dungeon bosses are assigned random Medallions or Spiritual Stones. However, there are _nine_ such items to distribute among only eight bosses. Because Link receives the Light Medallion for free upon becoming an adult in the original game, and because the cutscene where this event occurs has been removed, Link will start the game with a random Spiritual Stone or Medallion to compensate and add to the randomized experience. This item location is referred to as **Link's Pocket**.

Note that the Light Medallion, for all intents and purposes, is still just a worthless trinket.

### Items Not Shuffled
The following items are not shuffled and their locations are not part of any item pool:
- The Fairy Ocarina and Ocarina of Time
- Malon's Weird Egg
- Intermediate steps in the Child and Adult Trading Quest
- All shops
  - Medigoron will always sell the Giant's Knife
  - Business Scrubs, excluding the three which sell _unique upgrades_, will always sell what they advertise
  - The Happy Mask Shop is an integral part of the Child Trading Quest
- Gold Skulltulas themselves, including the tokens they hold
- Rewards you may obtain repeatedly (the replacement prizes when you win a minigame prize for the second time)
- Freestanding Rupees or Recovery Hearts

### Progressive Items
Certain types of items are modified to be _progressive_, meaning finding multiple instances will upgrade the item.

| Name in Spoiler | Collect One | Collect Two | Collect Three |
| ---:| --- | --- | --- |
| Slingshot | Slingshot + Bullet Bag | Big Bullet Bag | Biggest Bullet Bag |
| Bow | Bow + Quiver | Big Quiver | Biggest Quiver |
| Bomb Bag | Bomb Bag | Big Bomb Bag | Biggest Bomb Bag |
| Progressive Strength Upgrade | Goron Bracelet | Silver Gauntlets | Golden Gauntlets |
| Progressive Hookshot | Hookshot | Longshot | |
| Progressive Scale | Silver Scale | Golden Scale | |
| Progressive Wallet | Adult's Wallet | Giant's Wallet | |
| Magic Meter | Magic Meter | Double Magic | |
| Deku Stick Capacity | Hold 20 Sticks | Hold 30 Sticks | |
| Deku Nut Capacity | Hold 30 Nuts | Hold 40 Nuts | |

# Changes to Gameplay

### Shortened/Removed Cutscenes and Instant Text
A great effort has been made to cut out as much idle time as possible from the original game. Cutscenes are drastically shortened and where possible are removed entirely. Kaepora Gaebora will never interrupt you for an annoyingly long monologue that can be accidentally restarted. Text is written much faster. These changes are cosmetic in nature but speed up gameplay immensely.

Kaepora Gaebora will still fly you back to Castle Town from Lake Hylia or to Kakariko Village from Death Mountain Trail should you choose to talk to him.

### Bug Fixes and Quality of Life Changes
Some things have been changed and some bugs have been fixed entirely in order to better facilitate gameplay and allow a more thorough randomization. Of note:
- Bugfix: Obtaining the Poacher's Saw will no longer lock the player out of the Deku Theater Mask of Truth reward
- Becoming Adult Link will not automatically equip Child Link with the Kokiri Sword.
- Sheik will no longer prevent Link from returning to childhood before obtaining the Forest Medallion.
- Princess Ruto will now never disappear from Jabu Jabu's Belly, as she is vital to some puzzles.
- The Castle Courtyard becomes sealed off after completing the events within, instead of seeing the Ocarina of Time be thrown into the moat.
- In the Fire Temple, one door lock was removed. This is necessary to allow the Megaton Hammer (or the single item which locks its access) to be placed anywhere _other than the Megaton Hammer chest_.
- To make menu navigation in the inventory easier, empty inventory slots may now be highlighted with the cursor. This also fixes an issue where certain item combinations would result in unselectable items.

# Logic Notes
The randomized item layout will test your knowledge of the game's intended mechanics and items. Items may even be used in new ways to perform actions which would never appear in a casual run. Keep these in mind:

### Child Notes
- Child Link can perform nearly every action with a Deku Stick that he can with the Kokiri Sword. However:
  - You must have a sword equipped in order to play the Fishing minigame.
  - Logic will not expect you to defeat Dead Hand in the Bottom of the Well until you own the Kokiri Sword. You may still defeat Dead Hand with careful use of Deku Sticks.
- You do not need a Slingshot to play the Child Shooting Gallery minigame.
- You DO need a Bomb Bag to play Bombchu Bowling or purchase Bombchus.
- Stopping the Rolling Goron in Goron City does nothing unless Link owns a Bomb Bag and stops him within the tunnel that the Rolling Goron's sign is placed in.
- Skull Kid will not purchase the Skull Mask from Link unless Link plays _Saria's Song_ for him first.
- The Running Man, who purchases the Bunny Hood from Link and thereby completes the Child Trading Quest, requires all three Spiritial Stones.
- Open the Door of Time simply by playing the Song of Time for it. You do not need to collect the Spiritual Stones. The Ocarina of Time itself is merely a cosmetic upgrade to the Fairy Ocarina and does not grant any special ability.
  - If you arrive at the Temple of Time via _Prelude of Light_, playing the Song of Time for the Door will not work. Walk out and back in to load the scene correctly and resolve the issue.
- Spawning the Ocarina of Time (and learning the song from it) requires all three Spiritual Stones in your possession. Stand in front of the closed drawbridge leading to Castle Town. (Entering Hyrule Field from Castle Town with all three Spiritual Stones will dump Link into the moat. You will need to climb out and stand on dry ground.)

### Adult Notes
- You may play the Adult Shooting Gallery in Kakariko Village without a Bow. However, you cannot receive the randomized prize without a Bow and will instead be rewarded with 50 Rupees.
- Learning a song from Sheik at the Temple of Time requires that you own the Forest Medallion and visit as an adult.
- Learning a song from Sheik at Kakariko Village requires that you own the Forest, Fire, and Water Medallions, visit as an adult, and enter from Hyrule Field (not Graveyard or Death Mountain Trail).
- The Boulder Maze in Goron City requires Bombs to access the right side items, the Megaton Hammer to access either side, or the Silver Gauntlets to literally rip the maze apart. The Skulltula in the crate only exists as a child, so you will still need Bombs to access and kill it.
- If you have neither a Bomb Bag nor the Goron Bracelet, access to the lower sections of Death Mountain Crater (and therefore Sheik at the broken bridge and the Fire Temple) may be performed in the following alternative ways:
  - Detonate the Bomb Flower using a Bow to stop Link the Goron. This opens Darunia's chamber and lets you use his secret exit.
    - Due to an oversight in the logic, the Bow is not considered in accessing the lower crater, only for stopping Link the Goron.  
      - The two are considered separately; Link the Goron does not gate access to the lower crater. If your only access to stopping Link the Goron is the Bow, entering the Crater afterwards is out of logic and may not contain immediate progression.
    - You may also use a Bombchu, or detonate the Bomb Flower with Din's Fire or (hilariously enough) Blue Fire, to stop Link the Goron, though these methods are not considered in logic. 
  - Enter Death Mountain Crater from the top and use the Hover Boots to cross the gap to the left.
  - Enter Death Mountain Crater from the top and use the Longshot and Scarecrow's Song to navigate the route to the right. You will need the Megaton Hammer in this case in order to climb Death Mountain Trail.
- The Longshot is not necessary to perform any of the rooftop actions in Kakariko Village. The Hookshot is sufficient.
- The Longshot _is_ necessary to reach the Fire Arrows item, though you do not need to defeat Morpha to do so. Play the _Scarecrow's Song_ after walking down from the warp pad toward the island pillar, but before you fall into the bottom of the lakebed.
- Surprisingly, the game checks for the Goron Bracelet in the following places as an adult:
  - Bomb Flowers require the Goron Bracelet to be lifted.
  - The large colored blocks with the crescent moon and star symbol (for example, those in Forest Temple's Block Room) require the Goron Bracelet to be pushed.

### Other Notes
- Bombable Grottos may be opened with either Bombs, Bombchus, or the Megaton Hammer.
- If you are required to use a magic item to progress (Fire Arrows, Light Arrows, Din's Fire, or the Lens of Truth), you will also need to find Magic.
- While you can bypass the waterfall entry to Zora's Domain using a Cucco as a child or the Hover Boots as an adult, these are never considered in logic.
- The Lens of Truth is always considered for every fake wall and invisible object, including Bongo Bongo. It is also considered for the Treasure Minigame, as the Lens of Truth can reveal the winning choices to make. You will never be expected to pass through a fake wall, open an invisible chest, or play the Treasure Minigame until you own the Lens of Truth.
  - The exception to the rule is the Bottom of the Well, where the player is expected to walk through the initial fake wall to enter the dungeon, which is where the Lens of Truth is located in the original game.
- Learning a song from Sheik at the Desert Colossus may be done as an adult or as a child. Simply enter and exit Spirit Temple.

### Dungeon-Specific
- The Song of Time can summon and dispel the blue blocks featuring the Door of Time symbol. Remember that these blocks can be summoned to climb to new areas in the Fire Temple's final Goron jail, Gerudo Training Grounds Lava Rupees room, and Ganon's Castle Shadow Trial.
- The Fire Temple and Water Temple expect that Link owns the Goron Tunic and Zora Tunic, respectively. You may be expected to find one in the item pool before entering, or you may be expected to purchase one.
  - Purchasing the Goron Tunic (200 Rupees) requires an Adult Wallet (200 Rupees) and a way to stop Link the Goron (Bombs, Goron Bracelet, or the Bow).
  - Purchasing the Zora Tunic (300 Rupees) requires a Giant's Wallet (500 Rupees), a source of Blue Fire (300 Rupees, if purchased in the Potion Shop), a Bottle to hold the Blue Fire in, and Zelda's Lullaby in order to access Zora's Domain as an adult.
  - It is possible to _lose_ your Tunic to a Like-Like and not be able to purchase a new one. In the case of the Zora Tunic, this may not be detrimental. In the case of the Goron Tunic, this may make life incredibly difficult. Please be careful.

#### Dodongo's Cavern
- Adult Link can fully clear Dodongo's Cavern. Some things to note:
  - Dodongo's Cavern is open automatically as an adult. No need to bomb the entrance!
  - Link still needs the Goron Bracelet to lift Bomb Flowers, even as an adult.
  - The Megaton Hammer will break all bombable walls in Dodongo's Cavern.
  - Adult Link can skip the first floor loop path by jumping directly to the floor switch from the lobby.
    - Child Link can perform the same skip by using a Ground Jump (an [easy to perform glitch](http://zelda.speedruns.com/oot/tech/ground-jump)), though this is not in logic.
  - The Bow or Din's Fire are acceptable substitutes for blasting the stone staircase to reach the second floor.
    - Hilariously, Blue Fire also works, though you will need two bottles of it and this method is not in logic.
  - The second floor loop through the upper miniboss fight and fire pillars may be skipped entirely as an adult.
    - The in-logic method is to use the Hover Boots upon first entering the Bomb Bag Room.  
      Hover to the left instead of dropping down and you will grab on to a pillar.
    - This pillar may be jumped to without the use of Hover Boots, though this is not in logic.
  - Bombchus may be used to light up the skull's eyes. However, Bombchus are not in logic here.
  - Yes, Bombchus may be used to defeat King Dodongo as an adult using a [particular Ground Jump setup](https://youtu.be/scZnFD1hB7E?t=650).  
    However, this is not considered in logic and not recommended for inexperienced players.

#### Forest Temple
- Remember that you will need _Saria's Song_ or _Minuet of Forest_ to reach the Sacred Forest Meadow, then Hookshot to enter.
- You will need the Bow or the Song of Time in order to enter the courtyards from the lobby.
- You will also need the Goron Bracelet in order to complete the dungeon, as Link cannot push large blocks without it.
- If you do not have the _Song of Time_, don't despair! You can still access both courtyards with an assortment of other items.
  - As should be obvious, the Bow will grant you access to the right courtyard.
  - From the large block pushing room, you can reach the left courtyard balcony (with the door leading to the Floormaster).  
    You will need the Hover Boots to do so in-logic, and one key in order to enter the block room.
    - If you do not have a Bow or the _Song of Time_, this may be your only access to the courtyards.
  - You may cross from the right courtyard to the left courtyard via the well using Iron Boots or Golden Scale.
  - You may cross from the right courtyard to the left courtyard via Map Chest Room using the Longshot to latch on to high-up vines near the switch that drains the well.

#### Fire Temple
- You are not expected to enter Fire Temple before first owning a Goron Tunic.
- There are multiple methods to reach Fire Temple.
  - The most common method is to cross the broken bridge. This may be initially reached by:
    - Stopping _Link the Goron_, which requires one of the following: Goron Bracelet, Bombs, Bow.
      - Out-of-logic methods to stop Link the Goron: Bombchu, Din's Fire, Blue Fire.
      - Due to an oversight in the logic, the Bow is not considered in accessing the lower crater, only for stopping Link the Goron.  
        - The two are considered separately; Link the Goron does not gate access to the lower crater. If your only access to stopping Link the Goron is the Bow, entering the Crater afterwards is out of logic and may not contain immediate progression.
    - Using Hover Boots to cross from the upper part of Death Mountain Crater and grab on to the ledge.
    - Crossing the broken bridge itself requires Hookshot or Hover Boots.
  - Much less common is to be required to use the Longshot and _Scarecrow's Song_ to travel counter-clockwise around the crater,  
    and the Megaton Hammer to climb Death Mountain Trail in the first place.
  - _Bolero of Fire_ may be used to reach Fire Temple with no other prerequisite.
- Additionally, you will need Bombs to fully clear the dungeon, and the Megaton Hammer to defeat Volvagia.
- You will also need the Goron Bracelet in order to complete the dungeon, as Link cannot push large blocks without it.
  - In this case, there is only one such large block, in the room above the block elevator (which Link can push easily).  
    A Ground Jump (an [easy to perform glitch](http://zelda.speedruns.com/oot/tech/ground-jump)) will bypass this block, though this method is not in logic.
- You can reach the Boss Key door from the beginning with Hover Boots. This is in logic, and Volvagia may hold a Small Key.
- There is one extra key in Fire Temple. This is because one door lock is removed in the lobby, behind the hammer totem.
- Speaking of keys, you can skip using one in the Fire Maze if you have Hover Boots and Megaton Hammer.  
  Simply cross from the room entrance to the final hammer pillar, then hammer the rusted switch.

#### Water Temple
- While you're here, you don't need to defeat Morpha to reach the Fire Arrows item. Play the _Scarecrow's Song_ after walking down from the warp pad toward the island pillar, but before you fall into the bottom of the lakebed.
- You are not expected to enter Water Temple before first owning a Zora Tunic.
- You will need the Hookshot and Iron Boots in order to enter Water Temple. Fully clearing Water Temple requires the Bow and Longshot.
- You may travel up and down the central tower's exterior with the water fully lowered. Stand near the inner wall, use your Hookshot  
  to hit the next target up, and jumpslash to land on the next level up.
  - This means you do not strictly need to use a key in order to enter the central tower, as with the water level lowered there is a  
    lit torch that you can shoot an arrow through to unlock the second floor entrance to the central tower.
  - You can use this to ascend to the top level, though this is only helpful if you need to raise the water level fully.
    - To do so without spending a key, you will need to use Hover Boots _or_ a rolling jump aimed toward the _left_ side of the ledge where the water level station is located. The jump without Hover Boots is considered in logic.
- Hover Boots can be used to reach the Boss Key chest without going through the room that requires Bombs and block pushing.  
  Simply hover to the hole to the left where boulders roll from.
- Hover Boots can also be used to pass the eye switch in the central hub's second level without using the Longshot.

#### Shadow Temple
- You will need the _Nocturne of Shadow_ to reach Shadow Temple, and all of the following to be granted in-logic access:  
  Din's Fire, Lens of Truth, and _either_ Hookshot or Hover Boots.
- You will also need the Goron Bracelet in order to reach every item check in the dungeon, as Link cannot push large blocks without it.
  - The dungeon may be completed without the use of the Goron Bracelet if the upper chests in Spike Trap room do not contain keys.
  - The block normally used to reach the ferry boat may be bypassed by using the Hookshot on the ladder.
- If you do not have Hover Boots, there are only two item locations in Shadow Temple accessible to you.
- In the Invisible Spikes room, you do not need the Longshot to reach the locked door. Backflip onto the room's chest for height.
- You may cross the large chasm after the ferry boat using the Longshot and _Scarecrow's Song_ instead of the Bow.
  - [A well-aimed Bombchu can also be used to detonate the bomb flowers](https://www.twitch.tv/videos/299938965), though this method is not in logic.

#### Spirit Temple
- Rejoice, Bombchu fans! Your faithful little explosive rodent companion is finally helpful. But... still not demanded in logic.
- Reaching the Spirit Temple can be an ordeal in itself.
  - You may skip the entire sequence if you possess the _Requiem of Spirit_.
  - If you do not, you will need to take the long route. This means the following somewhat extensive list:
    - Epona _or_ the Longshot to cross the broken Gerudo Valley bridge
    - Completion of the Carpenter rescue to gain access to the Haunted Wasteland
    - Longshot _or_ Hover Boots to cross the quicksand in the Haunted Wasteland
    - Lens of Truth to follow the Poe guide that leads you through the desert to the Desert Colossus
- Remember to exit the Spirit Temple as soon as you enter it. This triggers Sheik's song check here as an adult _or_ as a child.
- Child notes:
  - You may kill the Armos using a Deku Stick. This is accounted for.
  - You will need the Boomerang or Slingshot to make the initial circuit for the two child-exclusive item locations.
    - You may substite Bombchus by sending one directly up the wall opposite the falling bridge.  
      Detonate it with a Deku Nut if you fear you've overshot. This is not in logic.
  - Child Link can activate the Map Chest in the central statue room using a Deku Stick. No magic needed!
- Adult notes:
  - The Hover Boots are not strictly required in the Spirit Temple.
    - You may complete the rolling boulder Silver Rupees with a jumpslash.
    - You may jump to the statue's hands from above.
    - The Hover Boots can be used to reach the upper platforms, but this is _not_ considered in logic.
  - Playing Zelda's Lullaby in the statue's hand spawns _two_ chests, not just one! The second is in the northeast corner at the top.
  - You can use the Longshot to cross from Mirror Shield Chest to Silver Gauntlets Chest. This is considered in logic.
  - Spirit Temple has two invisible chests. Thankfully, both are in one room and both are very close together.
  
#### Ganon's Castle  
- The one place in the randomizer where Bombchus are _demanded_ in logic. No other glitchless method allows completion of Spirit Trial.
- In Spirit Trial, the web on the ceiling may be burned by Fire Arrows or, less obviously, a normal arrow through a nearby torch. Din's Fire simply will not reach.
- In Shadow Trial, magical fire may be skipped entirely by using the Longshot to cross to the Like-Like, then Hover Boots over the gap.
- There is free Blue Fire in the Water Trial. You may very well be required to use this Blue Fire source to unfreeze King Zora.

# Known issues

Sadly for this 2.0 release a few known issues exist. These will hopefully be addressed in future versions.

-The fishing minigame sometimes refuses to allow you to catch fish when playing specifically on Bizhawk. Save and quit (NOT savestate) and return to fix the issue.  
-Draining the Bottom of the Well with Song of Storms sometimes crashes on specific configurations of Project 64. We aren't sure of the exact story, but this bug is
easily avoided by playing on a different emulator and probably also avoidable by changing your settings and maybe graphics plug-in.  
-There's a funny bug where sometimes obtaining Biggoron Sword displays a second erroneous text box. This has no gameplay consequence.  
-Executing the collection delay glitch on various NPCs may have unpredictable and undesirable consequences. In particular this can be devastating with Biggoron;
it is strongly suggested the player save before turning in the Claim Check.  
-Saving and quitting on the very first frame after becomming an adult when you would trigger the Light Arrow cutscene can have undesired consequences. Just don't
do that.  

# Settings

## Rainbow Bridge

This determines the condition under which the rainbow bridge to Ganon's Castle will spawn.

### Medallions

All six of the medallions are required to open Ganon's Castle.

### Vanilla

The rainbow bridge spawns under the same conditions it did in the original game, possession of the Light Arrows and having viewed the Zelda cutscene.

### All Dungeons

The rainbow bridge spawn requires all medallions and spiritual stones to be in the player's possession.

### Open

The rainbow bridge is always present.

## Kokiri Tunic Color

This determines the color of Link's default Kokiri Tunic. This only affects the color when he's wearing it, not the color of the icon in the menu.

### Most Colors

Simply get the particular color selected. Available colors are Kokiri Green, Goron Red, Zora Blue, Black, White, Purple, Yellow, Orange, Pink, Gray,
Brown, Gold, Silver, Beige, Teal, Royal Blue, Sonic Blue, Blood Red, Blood Orange, NES Green, and Dark Green.

### Random

Choose a random color from the set of pre-made colors.

### True Random

Generate a random color with numerically random RGB values.

## Goron Tunic Color

This determines the color of Link's Goron Tunic. This only affects the color when he's wearing it, not the color of the icon in the menu or when
holding it up after acquiring it. The options are identical to those for the Kokiri Tunic.

## Zora Tunic Color

This determines the color of Link's Zora Tunic. This only affects the color when he's wearing it, not the color of the icon in the menu or when
holding it up after acquiring it. The options are identical to those for the Kokiri Tunic.

## Low Health SFX

This determines which sound effect to play repeatedly when Link is very low on health. Several of these options are designed to be potentially
more pleasant to listen to while a few are designed to be more amusing.

### Particular Sounds

Set this particular sound for the heart beep. Available choices are Default, Softer Beep, Rupee, Timer, Tamborine, Recovery Heart, Carrot Refill,
Navi - Hey!, Zelda - Gasp, Cluck, and Mweep!. The last of these is indeed the sound a king might make when moving... very slowly.

### None

Disable low health heart beeps altogether.

## Create Spoiler Log

Output a Spoiler File.

## Do not Create Patched Rom

If set, will not produce a patched rom as output. Useful in conjunction with the spoiler log option to batch
generate spoilers for statistical analysis.

## Compress patched Rom

If set, the randomizer will additionally output a compressed ROM using Grant Man's bundled compressor. This compressor is the fastest
compressor out there and tuned specifically for this game, but in order to achieve its incredibly high speed, it does utilize every last bit
of CPU your computer will give it so your computer will slow to a crawl otherwise during the couple of minutes this will take.

## Open Forest

Mido does not need to see a sword and shield to reach the Deku Tree and the Kokiri boy blocking the exit to the forest is gone.
If this flag is not set, it is guaranteed that the Deku Tree can be completed without leaving the forest.

## Open Door of Time

The Door of Time is open from the beginning of the game. The Song of Time is only useful to move Song of Time blocks.

## Skip most of Ganon's Castle

The barrier protecting Ganon's Tower within Ganon's Castle is dispelled from the start, the Boss Key doors within Ganon's Tower are unlocked by
default, Ganondorf will provide a hint for the location of Light Arrows, and the collapsing tower sequence is skipped.

## Place Dungeon Items

If not set, Compasses and Maps are removed from the dungeon item pools and replaced by five rupee chests that may end up anywhere in the world.
This may lead to different amount of itempool items being placed in a dungeon than you are used to.

## Only Ensure Seed Beatable

If set, will only ensure that Ganon can be defeated, but not necessarily that all locations are reachable.

## Gossip Stone Hints with Stone of Agony

If set, the 32 Gossip Stones scattered across Hyrule will have various hints informing the player of which items are in various inconvenient locations. The
Stone of Agony is the condition to be able to talk to the Gossip Stones in this mode instead of the Mask of Truth out of mercy to the player. The nine locations
we regarded as the most generally inconvenient for all medallions play will always have hints, those hints will appear in two places, and the logic will guarantee
access to the Stone of Agony before those places must be checked. Those places are the rewards for 30, 40, and 50 Gold Skulltullas, both rewards from the fishing
minigame, the song from the Ocarina of Time, the item from showing the Mask of Truth in the Deku Theater, the item for defeating 10 Big Poes, and the item for
redeeming the Claim Check with Biggoron. There will be seven other hints that only exist once for other somewhat inconvenient places for which there is no
guarantee of Stone of Agony access, and there will be seven other sorts of remarks from the Gossip Stones in the hint pool that may bring a smile to your face but
will not provide you with unique information for your quest. The unreachable Gossip Stone in the Kokiri Forest is included in this 32 Gossip Stone hint shuffle as
well so be aware that one instance of a hint will seem to effectively vanish every seed.

## Seed

Can be used to set a seed number to generate. Using the same seed with same settings on the same version of the randomizer will always yield an identical output.

## Count

Use to batch generate multiple seeds with same settings. If a seed number is provided, it will be used for the first seed, then used to derive the next seed (i.e. generating 10 seeds with the same seed number given will produce the same 10 (different) roms each time).

# Command Line Options

```
-h, --help            
```

Show the help message and exit.

```
--create_spoiler      
```

Output a Spoiler File (default: False)

```
--bridge [{medallions,vanilla,dungeons,open}]
```

Select the condition to spawn the Rainbow Bridge to Ganon's Castle. (default: medallions)

```
--kokiricolor [{'Kokiri Green', 'Goron Red', 'Zora Blue', 'Black', 'White', 'Purple', 'Yellow', 'Orange', 'Pink', 'Gray', 'Brown', 'Gold', 'Silver', 'Beige', 'Teal', 'Royal Blue', 'Sonic Blue', 'Blood Red', 'Blood Orange', 'NES Green', 'Dark Green', 'Random', 'True Random'}]
```

Select the color of Link's Kokiri Tunic. (default: Kokiri Green)

```
--goroncolor [{'Kokiri Green', 'Goron Red', 'Zora Blue', 'Black', 'White', 'Purple', 'Yellow', 'Orange', 'Pink', 'Gray', 'Brown', 'Gold', 'Silver', 'Beige', 'Teal', 'Royal Blue', 'Sonic Blue', 'Blood Red', 'Blood Orange', 'NES Green', 'Dark Green', 'Random', 'True Random'}]
```

Select the color of Link's Goron Tunic. (default: Goron Red)

```
--zoracolor [{'Kokiri Green', 'Goron Red', 'Zora Blue', 'Black', 'White', 'Purple', 'Yellow', 'Orange', 'Pink', 'Gray', 'Brown', 'Gold', 'Silver', 'Beige', 'Teal', 'Royal Blue', 'Sonic Blue', 'Blood Red', 'Blood Orange', 'NES Green', 'Dark Green', 'Random', 'True Random'}]
```

Select the color of Link's Zora Tunic. (default: Zora Blue)

```
--healthSFX [{'Default', 'Softer Beep', 'Rupee', 'Timer', 'Tamborine', 'Recovery Heart', 'Carrot Refill', 'Navi - Hey!', 'Zelda - Gasp', 'Cluck', 'Mweep!', 'Random', 'None'}]
```

Select the sound effect that loops at low health. (default: Default)

```
--rom ROM
```

Path to a The Legend of Zelda: Ocarina of Time NTSC-US v1.0 ROM. (default: ZELOOTROMDEC.z64)

```
--loglevel [{error,info,warning,debug}]
```

Select level of logging for output. (default: info)

```
--seed SEED           
```

Define seed number to generate. (default: None)

```
--count COUNT         
```

Set the count option (default: None)

```
--open_forest
```

Set whether Kokiri children obstruct your path at the beginning of the game. (default: False)

```
--open_door_of_time
```

Set whether the Door of Time is open from the beginning of the game. (default: False)

```
--fast_ganon
```

Set whether most of Ganon's Castle can be skipped. (default: False)

```
--nodungeonitems
```

If set, Compasses and Maps are removed from the dungeon item pools and replaced by five rupee chests that may end up anywhere in the world.
This may lead to different amount of itempool items being placed in a dungeon than you are used to. (default: False)

```
--beatableonly
```

Enables the "Only Ensure Seed Beatable" option (default: False)

```
--hints
```

Gossip Stones provide helpful hints about which items are in inconvenient locations if the Stone of Agony is in the player's inventory. (default: False)

```
--suppress_rom
```

Enables the "Do not Create Patched Rom" option. (default: False)

```
--compress_rom
```

Create a compressed version of the output ROM file. (default: False)

```
--gui
```

Open the graphical user interface. Preloads selections with set command line parameters.
