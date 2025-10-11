# Legacy Track

## Description
A small Minecraft Java resource pack containing a .json file that remaps all music sound events to play C418 music like how it is on the legacy editions of Minecraft.
</p>
<br>

<p align="center">
  <img src="https://ia601804.us.archive.org/20/items/minecraft-volume-alpha/Cover.jpg?cnt=0" width="250">
</p>
<p align="center">
  Image Credit: C418 Alpha Volume Album Cover
</p>
<br>

## Installation
1. Navigate to the releases on the right to download the specified release version. You should be getting a zip file containing the files found in this repository.
2. Navigate to the resource packs folder in your minecraft directory (.minecraft/resourcepacks) and put the zip file there.
3. In the game, navigate to the resource packs menu and load the resource pack (it is recommended to put the resource pack at the top of the list of loaded resource packs).

## Supported Versions
`Java 1.21.8`

## How it works
Sound events are used in Minecraft to indicate what sound file to use (e.g.: on creative mode, the music.creative sound event is used to play background music that belongs to that event). 
There are sound events for background music that are triggered based on the corresponding events:
* User Interface
  * music.menu
  * music.credits
* Game Mode
  * music.creative
  * music.game
* Dimension
  * music.end
* Gameplay
  * music.dragon
  * music.underwater
* Biome
  * music.overworld.badlands
  * music.overworld.cherry_grove
  * music.overworld.desert
  * music.overworld.forest
  * music.overworld.frozen_peaks
  * music.overworld.grove
  * music.overworld.jagged_peaks
  * music.overworld.jungle
  * music.overworld.lush_caves
  * music.overworld.meadow
  * music.overworld.old_growth_taiga
  * music.overworld.snowy_slopes
  * music.overworld.sparse_jungle
  * music.overworld.stony_peaks
  * music.overworld.swamp
  * music.nether.basalt_deltas
  * music.nether.crimson_forest
  * music.nether.nether_wastes
  * music.nether.soul_sand_valley
  * music.nether.warped_forest

The .json file provided redefines these sound events with their own sounds list to play specifically C418 music.

### Examples:

#### User Interface:
<table>
<tr>
<th>Vanilla</th>
<th>Legacy Track</th>
</tr>
<tr>
<td>
  
```json
"music.menu":
{
  "sounds":
  [
    { "name": "music/game/below_and_above", "stream": true, "volume": 0.4 },
    { "name": "music/game/broken_clocks",   "stream": true, "volume": 0.4 },
    { "name": "music/game/fireflies",       "stream": true, "volume": 0.4 },
    { "name": "music/game/lilypad",         "stream": true, "volume": 0.4 },
    { "name": "music/game/os_piano",        "stream": true, "volume": 0.4 },
    { "name": "music/menu/beginning_2",     "stream": true },
    { "name": "music/menu/floating_trees",  "stream": true },
    { "name": "music/menu/moog_city_2",     "stream": true },
    { "name": "music/menu/mutation",        "stream": true }
  ]
}
```
  
</td>
<td>

```json
"music.menu":
{
  "replace": true,
  "sounds":
  [
    { "name": "music/menu/beginning_2",    "stream": true },
    { "name": "music/menu/floating_trees", "stream": true },
    { "name": "music/menu/moog_city_2",    "stream": true },
    { "name": "music/menu/mutation",       "stream": true }
  ]
}
```

</td>
</tr>

</table>

#### Gamemode:
<table>
<tr>
<th>Vanilla</th>
<th>Legacy Track</th>
</tr>
<tr>
<td>
  
```json
"music.creative":
{
  "sounds":
  [
    { "name": "music.game", "type": "event" },
    { "name": "music/game/creative/aria_math",    "stream": true },
    { "name": "music/game/creative/biome_fest",   "stream": true },
    { "name": "music/game/creative/blind_spots",  "stream": true },
    { "name": "music/game/creative/dreiton",      "stream": true },
    { "name": "music/game/creative/haunt_muskie", "stream": true },
    { "name": "music/game/creative/taswell",      "stream": true }
  ]
}
```
  
</td>
<td>

```json
"music.creative":
{
  "replace": true,
  "sounds":
  [
    { "name": "music/game/creative/aria_math",      "stream": true },
    { "name": "music/game/creative/biome_fest",     "stream": true },
    { "name": "music/game/creative/blind_spots",    "stream": true },
    { "name": "music/game/creative/dreiton",        "stream": true },
    { "name": "music/game/creative/haunt_muskie",   "stream": true },
    { "name": "music/game/creative/taswell",        "stream": true }
  ]
}
```

</td>
</tr>
</table>

#### Biome: 
<table>
<tr>
<th>Vanilla</th>
<th>Legacy Track</th>
</tr>
<tr>
<td>
  
```json
"music.overworld.bamboo_jungle":
{
  "sounds":
  [
    { "name": "music/game/bromeliad",         "stream": true, "volume": 0.4, "weight": 2 },
    { "name": "music/game/danny",             "stream": true },
    { "name": "music/game/dry_hands",         "stream": true },
    { "name": "music/game/haggstrom",         "stream": true },
    { "name": "music/game/key",               "stream": true },
    { "name": "music/game/left_to_bloom",     "stream": true, "volume": 0.4 },
    { "name": "music/game/living_mice",       "stream": true },
    { "name": "music/game/mice_on_venus",     "stream": true },
    { "name": "music/game/oxygene",           "stream": true },
    { "name": "music/game/subwoofer_lullaby", "stream": true },
    { "name": "music/game/wet_hands",         "stream": true }
  ]
}
```
  
</td>
<td>

```json
"music.overworld.bamboo_jungle":
{
  "replace": true,
  "sounds":
  [
    { "name": "music/game/clark",         "stream": true },
    { "name": "music/game/danny",         "stream": true },
    { "name": "music/game/dry_hands",     "stream": true },
    { "name": "music/game/haggstrom",     "stream": true },
    { "name": "music/game/key",           "stream": true },
    { "name": "music/game/living_mice",   "stream": true },
    { "name": "music/game/mice_on_venus", "stream": true },
    { "name": "music/game/minecraft",     "stream": true },
    { "name": "music/game/wet_hands",     "stream": true },
    { "name": "music/game/oxygene",       "stream": true },
    { "name": "music/game/sweden",        "stream": true },
    { "name": "music/game/wet_hands",     "stream": true }
  ]
}
```

</td>
</tr>
</table>



For all documentation about sound events and a list of all sound events along with their associated sound files and attributes, I highly recommend visiting the ![Minecraft Wiki](https://minecraft.wiki/w/Sounds.json#File_structure). Additionally, if you would like an updated json structure of sound events, visit ![MCA Explorer](https://mcasset.cloud/1.21.8/assets/minecraft/sounds.json).

## Notes
* Please refrain from posting issues regarding when the resource pack will be updated for a certain version of the game. I cannot guarantee when I will be updating the resource pack to a certain version of the game and will simply ignore/delete those issues. I will post to the issues tab of what update I will be updating the resource pack to.
* I decided to keep the deep dark and the new nether soundtrack since I found that they stay close to the theme of the biome/dimension.
* If there are any issues you come across, please don't hesitate to post the issue on the issues tab of the repository. I plan to address issues there.
* There is also no guarantee that a Bedrock version of this resource pack will be made. Like the updates, I will put an issue for making a Bedrock version of the resource pack to say that there will be one in the future.
* There may be incompatibilities with mods, datapacks, other resource packs, mod loaders, and game versions. Please let me know of them in the issues and I will see what I can do to fix the issues on my end.
