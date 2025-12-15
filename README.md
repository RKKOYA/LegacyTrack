</p>
<br>
<p align="center">
  <img width="300" height="300" alt="pack" src="https://github.com/user-attachments/assets/342526df-2cb8-4b3b-820e-37e639917154" />
</p>
<p align="center">
A pair of small resource packs that remaps all music sound events to play C418 music like how it is on the legacy editions of Minecraft. This project aims to only resource packs to accomplish this task.
</p>
<br>

<div align="center">
  
[![GitHub Downloads](https://img.shields.io/github/downloads/rkkoya/LegacyTrack/total?style=for-the-badge&logo=github&color=006ca5)](https://github.com/RKKOYA/LegacyTrack/releases)
[![Modrinth Downloads](https://img.shields.io/modrinth/dt/6Ptdj5WF?style=for-the-badge&logo=modrinth&color=008000)](https://modrinth.com/mod/legacytrack)

</div>

## Table of Contents
1. [Goals](#goals)
2. [Supported Game Versions](#supported-game-versions)
3. [Installation](#installation)
4. [How it Works](#how-it-works)
   - 4.1 [Examples](#examples)
        - 4.1.1 [User Interface](#user-interface)
        - 4.1.2 [Game Mode](#game-mode)
        - 4.1.3 [Biome](#biome)
5. [Copyright](#copyright)
6. [Foot Notes](#foot-notes)



## 1. Goals <a name="goals"></a>
The project aims to play the Minecraft background music as follows:
* Main Menu:
  * Beginning 2
  * Floating Trees
  * Moog City 2
  * Mutation
* Survival (every biome minus deepdark²):
  * Clark
  * Danny
  * Dry Hands
  * Haggstrom
  * Key
  * Living Mice
  * Mice on Venus
  * Minecraft
  * Wet Hands
  * Oxygene
  * Sweden
* Creative (every biome including underwater):
  * Aria Math
  * Biome Fest
  * Blind Spots
  * Dreiton
  * Haunt Muskie
  * Taswell
* Nether (every biome)
  * Chrysopoeia²
  * Rubedo²
  * So Below²
  * Dead Voxel²
  * Concrete Halls
  * Warmth
  * Ballad of the Cats
* Underwater (UNCHANGED for survival, CHANGED to creative music)
* End (UNCHANGED)

## 2. Supported Game Versions <a name="supported-game-versions"></a>
`Java 1.21.8`

## 3. Installation <a name="installation"></a>
1. Navigate to the releases on the right to download the specified release version. You should be getting a .zip file.
<img width="814" height="146" alt="assets" src="https://github.com/user-attachments/assets/37967931-c460-4e9b-afc9-cbb54a334a66" />

2. Unzip the .zip file and you should be getting a folder containing two zipped folders; one for LegacyTrack and the other for LegacyTrackC. Each zipped folder contains the necessary resource pack files.
<img width="500" height="182" alt="extract" src="https://github.com/user-attachments/assets/c1270ea5-315f-4d3b-8d34-8ba52f05467b" />

3. Move those two .zip folders over to the minecraft resourcepacks folder.

4. In the game, navigate to options -> resourcepacks and load LegacyTrack. In creative mode, load LegacyTrackC on top of LegacyTrack; unload LegacyTrackC when switching back to survival mode.
<table>
<tr>
<th>Survival</th>
<th>Creative</th>
</tr>
<tr>
<td>
<img width="614" height="166" alt="survivalmode" src="https://github.com/user-attachments/assets/11ce2eb3-8e84-45a0-9ba8-c3d476f3b791" />
</td>
<td>
<img width="619" height="271" alt="creativemode" src="https://github.com/user-attachments/assets/b65d1cc8-2b00-47a5-a333-82667eaf12e1" />
</td>
</tr>

</table>

## 4. How it works <a name="how-it-works"></a>
Sound events are used in Minecraft as of 1.21.8 to indicate what sound file to use (e.g.: in the badlands biome, the 'music.overworld.badlands' sound event is triggered). 
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

The resource packs provide .json files that redefines this sound events to specifically play music like how it is on legacy console editions.

### 4.1 Examples: <a name="examples"></a>

#### 4.1.1 User Interface: <a name="user-interface"></a>
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

#### 4.1.2 Gamemode:  <a name="game-mode"></a>
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

#### 4.1.3 Biome: <a name="biome"></a>
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



For all documentation about sound events and a list of all sound events along with their associated sound files and attributes, I highly recommend visiting the [Minecraft Wiki](https://minecraft.wiki/w/Sounds.json#File_structure). Additionally, if you would like an updated JSON structure of sound events, visit [Minecraft Assets Explorer](https://mcasset.cloud/1.21.8/assets/minecraft/sounds.json).

## 5. Copyright <a name="copyright"></a>
* All C418 soundtracks belong to [Daniel Rosenfield](https://en.wikipedia.org/wiki/C418).

## 6. Foot Notes <a name="foot-notes"></a>
1. Please refrain from posting issues regarding when the resource pack will be updated for a certain version of the game. I cannot guarantee when I will be updating the resource pack to a certain version of the game and will simply ignore/delete those issues. I will post to the issues tab of what update I will be updating the resource pack to.
2. I decided to keep the deep dark and the new nether soundtrack since I found that they stay close to the theme of the biome/dimension.
3. If there are any issues you come across, please don't hesitate to post the issue on the issues tab of the repository. I plan to address issues there.
4. There is also no guarantee that a Bedrock version of this resource pack will be made. Like the updates, I will put an issue for making a Bedrock version of the resource pack to say that there will be one in the future.
5. There may be incompatibilities with mods, datapacks, other resource packs, mod loaders, and game versions. Please let me know of them in the issues and I will see what I can do to fix the issues on my end.
