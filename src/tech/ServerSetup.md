[CustomSpawnFix]: ./Links.md#map-packages 'fixes zed classes in old maps scripted triggers'
[MapVoteFix v2]: <https://forums.tripwireinteractive.com/index.php?threads/mod-voting-handler-fix.43202/> 'the only working mapvote for KF1'

# General Info

Some maps can work in [Objective mode](../KFObjective.md) if you rename their prefix, aka `KF- / KFS- / TOY-` to `KFO-`.

* KF-Arcade-Mission-v2
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

Might be more, test yourself and report!

# Map Voting Setup

To make some of the older objective maps (mostly from [Story mode](../KFMode.md)) work, we have to use [CustomSpawnFix].
Following instructions will help you to configure your server to use that mutator only on the maps that actually require it.

If you don't have [MapVoteFix v2] for some strange reason:

* Install it.
* Play for a few games so `MapVoteHistory.ini` will be created.

If you have it:

* Add all your maps to map list using one of the methods.
  * **WebAdmin** -> Defaults tab -> Maps.
  * In `killingfloor.ini` fill both **Maps** and **DefaultMaps** sections.
* Open `MapVoteHistory.ini`, find maps that require [CustomSpawnFix] and fill `U=` fields like in this example:

```bash
H=(M="KF-SaarV7",P=9,S=5,G=,U="CustomSpawnFix.CustomSpawnFixMut")
```

* If some of the maps are missing from `MapVoteHistory.ini` - either play on them first or add them here manually.
