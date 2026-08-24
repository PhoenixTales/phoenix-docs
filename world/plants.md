# Plants & Mushrooms

Author: *flosha*, add date from old docs  
Last update: 20.08.2026


## Gothic (Release)

In Gothic, plants were, for the most part, divided into those regenerating health (short "hp reg") and those regenerating mana (short "mana reg"). Following this categorization we can list them as follows (internally, they followed the scheme `ItFo_Plants_[ID]`; for simplcities sake we ommit the prefixes and only list the IDs below): 

### HP Reg Plants

| DE            | Internal        | Effect | Note   |
|---------------|-----------------|--------|--------|
| Waldbeere     | berries_01      | +10 HP |        |
| Flammendorn   | flameberry_01   | +12 HP |        |
| Seraphis      | seraphis_01     | +14 HP |        |
| Velayis       | velayis_01      | +16 HP | unused |
| Bergmoos      | mountainmoos_01 | +18 HP |        |
| Grabmoos      | mountainmoos_02 | +20 HP |        |
| Nachtschatten | nightshadow_01  | +22 HP |        |
| Mondschatten  | nightshadow_02  | +24 HP |        |
| Orkblatt      | orcherb_01      | +26 HP |        |
| Eichenblatt   | orcherb_02      | +28 HP |        |
| Heilkräuter 1 | herb_01         | +30 HP |        |
| Heilkräuter 2 | herb_02         | +39 HP |        |
| Heilkräuter 3 | herb_03         | +49 HP |        |
| Sumpfkraut    | swampherb_01    |        |        |


#### Names and Meanings

Interestingly, the Nightshadow plant V1 (in the Sequel the internal name has been corrected to "Nightshade"), in the English version, is called *Solanaceae* ingame, and the Moonshadow (or "Moonshade" = Nightshade V2), in the English version, is called *Lunanaceae* ingame.  


### Poisonous Plants

| DE            | Internal        | Effect | Note   |
|---------------|-----------------|--------|--------|
| Trollkirsche  | Trollberrys_01  | -20 HP | unused |

All of these plants only impacted HP and had no other effects. From the woodberry to the swanp/healing herbs they all gave progressively more HP bonus in steps of +2, until bigger jumps in case of the last two healing herbs. These 15 plants can be divided into 6 categories: 
1. Berries
2. "Flowers" or "Thistles" (Seraphis/Velayis)
3. Moss
4. Nightshade Plants
5. "Leaves"
6. (Swamp) Herbs


### Mana Reg Plants

| DE              | Internal     | Effect   | Note   |
|-----------------|--------------|----------|--------|
| Blutbuchensamen | bloodwood_01 |  +5 Mana |        |
| Turmeichensamen | towerwood_01 | +10 Mana | unused |
| Rabenkraut      | RavenHerb_01 | +15 HP   |        |
| Dunkelkraut     | RavenHerb_02 | +20 Mana |        |
| Steinwurzel     | Stoneroot_01 | +25 Nana |        |
| Drachenwurzel   | Stoneroot_02 | +30 Mana |        |

The same principle as above, but only 6 instead of 15 plants and 3 instead of 6 categories:
1. (Mana) Seeds
2. (Mana) Herbs
3. (Mana) Roots


### Mushrooms

| DE          | Internal    | Effect | Note |
|-------------|-------------|--------|------|
| Höllenpilz  | mushroom_01 |        |      |
| Sklavenbrot | mushroom_02 |        |      |


## Gothic (Alpha)

| DE          | Internal    | Effect | Note |
|-------------|-------------|--------|------|
| Honigpilz   | ToDo        | ToDo   |      |
| Teufelspilz | ToDo        | ToDo   |      |
| Psi Wurzel  | -           | -      |      |


## Gothic Sequel

In the Sequel documentation on plants and alchemy by Nyul and Filler, a few of those plants were not mentioned, while apparently three additional ones were added. 

Not mentioned were the following:
* Seraphis/Velayis
* Grabmoos (?)
* Eichenblatt
* Sklavenbrot
* Blutbuchensamen/Turmeichensamen
* Dunkelkraut
* Drachenwurzel

And these have been added:
* Blutdistel (Blood Thistle)
* Silberfarn (Silver Fern)
* Königstrost (-)
* Blutfarn (Todo: Also mentioned somewhere in the scripts?)

While Seraphis as a name did no longer appear, the Blood Thistle used Seraphis' and Velayis' old model and texture. It could well be that some plants weren't removed or replaced, but rather renamed. If so, Seraphis or Velayis could be the scientific term (as used by Alchemists), while blood thistle would be the more common name. The visuals should not be considered to be final either. 

While there does not seem to be a real blood thistle - regular thistles very much have the color Seraphis comes with; we would only have to regard the purple berry texture that the middle part uses as a placeholder for a thistle blossom. If we would follow the example of Silverfern and Bloodfern, there could as well be a silver thistle (which actually exists) and a blood thistle, which would be the more rare variant.  

Some plants were meant to have a different effect in the Sequel: 
* ToDo


## Plant Distribution

As a matter of fact the game world of Gothic has been still almost completely empty (no items being distributed) in versions as late as v0.94. Plant items included. All of the plants items were added a few weeks before release in a hurry, as so many other things. Due to this the plants have been distributed randomly without following any rules. 

It was done so randomly and under so much time pressure, that the cave mushroom (Höhlenpilz) got renamed into hell mushroom (Höllenpilz) in order to "fix" the mistake of a level designer who had put it all over the surface in open light, instead of in caves and other dark places only. There simply was no time left to do things properly. 

The team behind the Gothic Sequel, Nyul and Filler in particular, wanted to fix all of these mistakes. They renamed the mushroom into Cave Mushroom again and started writing a small plant documentation with guidelines for plant distribution. They summarised their plans as follows (from the `Sequel Design Documentation`):  

> Die Pflanzen sollen nicht "wie in Gothic" mal hier und dort mitten auf dem Weg kreuz und quer durcheinander verteilt werden, sondern aufgrund dieser Verteilungsliste in bestimmten Gebieten in kleinen Gruppen verteilt werden.

> Locations nutzen die neben den Wegen liegen! Es gibt unglaublich viele Locations die der Spieler durch herumlaufen/klettern erreichen kann, die in GOTHIC leer waren. Der Spieler soll durch das Erreichen/entdecken  dieser Locations mit ein paar Pflanzen belohnt werden.		

> Das bedeutet allerdings nicht, das der Spieler "on_the_fly" nicht ein paar Pflanzen einsacken kann, weil er nur auf dem Weg läuft. Auch hier wird er fündig, aber das Gro der Pflanzen will gefunden werden! Pflanzen wachsen in Gruppen :) zu (mind)zwei - X(max) zusammen. (Inflation bedenken! Findet der Spieler 20 wertvolle Pflanzen an einer Location ist er reich!	

> Verteilungsrichtlinie: Je wertvoller die Pflanze desto weniger gibt es davon und desto versteckter ist die Pflanze.		

English Translation: 

> EN: Plants shouldn't "like in Gothic" be distributed messily here and there in the middle of the road, but they should be distributed based on this distribution list in particular small groups.

> Use locations that are on the side of the road! There are unbelievably many locations that the player can reach by running around or climbing, which were empty in GOTHIC. The player should be rewarded by reaching/discovering these locations. 

> This does not mean though, that the player cannot loot some plants "on_the_fly", as he only walks on the road. Here too he will find something, but the majority of plants wants to be found! Plants grow in groups :) at a minimum of two to X (max) together. (Consider inflation! If the player finds 20 valuable plants at one location he is rich!)

> Guiding Principle: The more valuable the plant, the less of it there is and the more hidden is the plant.

---

Todo: Add distribution list with distribution guidelines for each camp. 

---

## Naming Convention

In the item scripts of Gothic there is an extra file (plants.d) reserved for plants, but it was left empty. Instead all plant IDs were written into the food file and named `ItFo_Plant_[ID]`. It makes sense insofar as that the plants have been an afterthought and couldn't be properly implemented into an alchemy crafting mechanic as they planned; they therefore served no other purpose anymore but as food. The Sequel wanted to correct this shortcoming. Consequentally the plants scripts were moved and a new naming convention was introduced, which we'll follow: `ItPl_[ID]`.  
For Mushrooms we are using `ItMu_[ID]`. Since they even have an associated alpha talent (`Identify_Mushrooms`) and as there will be much more mushrooms than the two remaining in the release version, they are in a script file on their own (mushrooms.d).  

---

## Phoenix 

### Plants

| DE              | Internal             | Effect   | Note   |
|-----------------|----------------------|----------|--------|
| Waldbeere       | ItPl_WoodBerry_01    | +10 HP   |        |
| Flammendorn     | ItPl_FlameBerry_01   | +12 HP   |        |
| Trollkirsche    | ItPl_TrollBerry_01   | -20 HP   | unused |
| Seraphis        | ItPl_Seraphis_01     | +14 HP   |        |
| Velayis         | ItPl_Velayis_01      | +16 HP   | unused |
| Bergmoos        | ItPl_MountainMoss_01 | +18 HP   |        |
| Grabmoos        | ItPl_MountainMoss_02 | +20 HP   |        |
| Nachtschatten   | ItPl_NightShade_01   | +22 HP   |        |
| Mondschatten    | ItPl_NightShade_02   | +24 HP   |        |
| Orkblatt        | ItPl_OrcLeaf_01      | +26 HP   |        |
| Eichenblatt     | ItPl_OrcLeaf_02      | +28 HP   |        |
| Heilkräuter 1   | ItPl_Herb_01         | +30 HP   |        |
| Heilkräuter 2   | ItPl_Herb_02         | +39 HP   |        |
| Heilkräuter 3   | ItPl_Herb_03         | +49 HP   |        |
| Sumpfkraut      | ItPl_SwampHerb_01    |          |        |
| Blutbuchensamen | ItPl_BloodWood_01    |  +5 Mana |        |
| Turmeichensamen | ItPl_Towerwood_01    | +10 Mana | unused |
| Rabenkraut      | ItPl_RavenHerb_01    | +15 HP   |        |
| Dunkelkraut     | ItPl_RavenHerb_02    | +20 Mana |        |
| Steinwurzel     | ItPl_Stoneroot_01    | +25 Nana |        |
| Drachenwurzel   | ItPl_Stoneroot_02    | +30 Mana |        |


### Mushrooms

| DE          | Internal             | Effect | Note         |
|-------------|----------------------|--------|--------------|
| Waldpilz    | ItMu_WoodMushroom    | ?      | Comic        |
| Waldpilz 2  | ItMu_WoodMushroom_02 | ?      |              |
| Honigpilz   | ItMu_HoneyMushroom   | ?      | Alpha v0.56c       |
| Höhlenpilz  | ItMu_CaveMushroom    | ?      | Alpha/Sequel |
| Sklavenbrot | ItMu_CaveMushroom_02 | ?      |              | 
| Erzpilz     | ItMu_OreMushroom     | ?      | Comic        |  
| Teufelspilz | ItMu_DevilsMushroom  | ?      | Alpha v0.56c        | 


### Description & Distribution

Beeren:  
* Waldbeere: ...
* Flammendorn: ...
* Trollkirsche: ...

Disteln:  
* Silberdistel: ...
* Blutdistel: ...

Farn:  
* Silberfarn: ...
* Blutfarn: ...

Moose:  
* Bergmoos: ...
* Grabmoos: ...

Nachtschattengewächse:  
* Nachtschatten: "Er wächst in der Sonne, doch nur im Schatten der Nacht entfalten er seine magische Wirkung."  
* Mondschatten: ...

Blätter:  
* Orkblatt
* Eichenblatt

Sumpfkräuter / Heilkräuter:  
* Heilkraut 1: ...
* Heilkraut 2: ...
* Heilkraut 3: ...

Samen:  
* Blutbuchensamen: ...
* Turmeichensamen: ...

(Mana) Kräuter:  
* Rabenkraut: ...
* Dunkelkraut: ...

Wurzeln:  
* Steinwurzel: ...
* Drachenwurzel: ...

* Königstrost?

Waldpilze:  
* Waldpilz: Very common mushroom inside and nearby the forests of the colony, of red-brown colour, inspired by the Comic.  
* Honigpilz: A rare wood mushroom (there is about 1 Honey Mushroom on 20 wood mushrooms), that only grows near bee hives; if a bee hive is spotted, the player can assume honey mushrooms to be near and when he spots a honey mushroom, he can assume to have a bee hive nearby. Based on the mushroom of the same name from v0.56c. 
* Teufelspilz: Very rare mushroom, poisonous on touch. About ~3 at most on the Colony Surface and ~3 underground. Based on the mushroom of the same name from v0.56c. 

Dunkelpilze:  
* Höhlenpilz: ...
* Sklavenbrot: ...
* Erzpilz: Poisonous cave mushroom, a Phoenix addition, based on the Comic.



