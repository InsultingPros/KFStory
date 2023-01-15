[Github Issues]: <https://github.com/InsultingPros/KFStory/issues>

[CustomSpawnFix]: <https://forums.tripwireinteractive.com/index.php?threads/mutator-customspawnfix.102956/> 'fixes zed classes in old maps scripted triggers'

[ScrnStoryGame]: <https://www.mediafire.com/file/sf1rm5e688dp9jt/ScrnStoryGame.zip/file>
[FoundryObj]: <https://www.mediafire.com/file/6tpf11xsf7p9bg9/FoundryObj.zip/file>
[KFChaingunTurret]: <https://www.mediafire.com/file/a0t0ypyd5wbbprt/KFChaingunTurret.zip/file>
[Fall_TriggerPack]: <https://www.mediafire.com/file/iyqot9pefdfcub3/Fall_TriggerPack.zip/file>
[KFGasCan]: <https://www.mediafire.com/file/p0d5acpbcunk7sw/KFGasCan.zip/file>
[clientmaterialtrigger]: <https://www.mediafire.com/file/x3ekplflstb3fc8/clientmaterialtrigger.zip/file>

[NetReduce]: <https://forums.tripwireinteractive.com/index.php?threads/utility-de-serverpackage-listing.103071/> 'hack of ol hacks to reduce serverpackage size'
[NetReduceSE]: <https://steamcommunity.com/groups/ScrNBalance/discussions/6/610575007209675730/> 'same thing but with config file'

[MapVoteFix v2]: <https://forums.tripwireinteractive.com/index.php?threads/mod-voting-handler-fix.43202/>

[DMN666]: <http://steamcommunity.com/profiles/76561198058194020>
[atagene]: <https://www.deviantart.com/atagene>

> Map lists are **HUGE**, a lot of days were spent sorting files, creating categories and filling in all the information in the right places. So there can be typos, missing maps, links, credits and false information. If you find any please let us know: [Github Issues].

## General Info

Ola! I adore **Killing Floor 1** story maps and greatly respect all the work, time that their authors put into their creations. So I aimed to create a place where everyone can easily find, compare, download and install any map in a few clicks. Enjoy.

* Maps are categorized by gametypes (map prefixes).
* Most useful, not broken maps are on top of the list. Yeah I sorted them by my taste, v52.
* All archives have **redirect** (*.uz2) files in them. Don't thank me.
* All archives are made by [7zip](https://www.7-zip.org/) with following settings:
  * Archive format:       zip
  * Compression level:    Ultra
  * Compression method:   Deflate
  * Dictionary size:      32 KB
  * Word size:            258

This allow archives to be opened in windows explorer. I could go for `*.rar` or `*.7z` instead, but size savings are not that significant, and end users must have 3rd party apps to open them. So not worth it imo.

* All list entries follow the same format:
  * **Title**: map name.
  * **Authors**: one or more, with [links to user accounts](./Links.md#map-authors) (if there are any).
  * **Map filename**: with prefix ofc.
  * **Links**: starting from DL then Workshop, Forum, ModDb, Site (if there are any).
  * **Notes**: a special section for greylisted maps or when I need to warn you about game breaking stuff / [CustomSpawnFix].
  * **Clickable screenshots**: to easily recognize the maps. Except some old, exported JPG's, these are [TinyPNG](https://tinypng.com/) optimized PNG's.

Some maps can work in [Objective mode](./KFObjective.md) if you rename their prefix, aka `KF- / KFS- / TOY-` to `KFO-`.

* kf-Arcade-Mission-v2
* KF-Hokuto_Ujou_Hagan_Ken_v2
* KF-LaserChallengeV3
* KF-Offices-Story-alpha1
* KF-roofhop
* KF-SaarV5
* KF-Strangev12
* KF-TheHiveV1REV3
* KF-TheHiveV2FC
* KF-TheHiveV3Beta
* TOY-DevilsDollhouse
* TOY-DevilsDollhouse-FixV3
* might be more, test yourself.

## Map Packages

> Always keep [CustomSpawnFix] around, it will help greatly if you have invisible zeds. Thanks Tripwire for renaming zed classes in latest patches and breaking old story maps.

> Avoid [NetReduce] and [NetReduceSE] at all costs, or you will get broken spawns, pickups, missing keys, switches, etc etc.

These packages are **Whitelisted**, if you see them don't worry:

* [ScrnStoryGame] - adds many and many additional scripts, npc support, dialogues, etc.
* [FoundryObj] - a bit more scripts ^.
* [KFChaingunTurret] - a usable gatling gun.
* [Fall_TriggerPack] - one of the oldest ones around, has few useful triggers.
* [KFGasCan] - gas can and related scripts.
* [clientmaterialtrigger] - allows to change materials for clients.

## Server Setup

To make some of the older objective maps (mostly from [Story mode](./KFMode.md)) work, we have to use [CustomSpawnFix].
Following instructions will help you to configure your server to use that mutator only on the maps that actually require it.

If you don't have [MapVoteFix v2] for some strange reason:

* Install it.
* Play for a few games so `MapVoteHistory.ini` will be created.

If you have it:

* Add all your maps to map list using one of the methods.
  * **WebAdmin** -> Defaults tab -> Maps.
  * In `killingfloor.ini` fill both **Maps** and **DefaultMaps** sections.
* Open `MapVoteHistory.ini`, find maps that require [CustomSpawnFix] and fill `U=` fields like in this example:

```clike
H=(M="KF-SaarV7",P=9,S=5,G=,U="CustomSpawnFix.CustomSpawnFixMut")
```

* If some of the maps are missing from `MapVoteHistory.ini` - either play on them first or add them here manually.

## Credits

**[DMN666]**: his original [thread](https://forums.tripwireinteractive.com/index.php?threads/kf-game-modes-and-maps.101777/) helped me a lot when I started this project. Without him this thread wouldn't exist.

**KillingFloor.ru** and staff: this forum was a great host for my initial [thread (Wayback Machine)](https://web.archive.org/web/*/http://killingfloor.ru/xforum/threads/kf-story-gametypes-i-karty-k-nim.4219/).

**[atagene]**: thanks for a nice [logo](https://www.deviantart.com/atagene/art/Killing-Floor-Text-522558359)!
