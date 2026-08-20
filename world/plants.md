# Plants

Author: *flosha*, add date from old docs
Last update: 20.08.2026


In Gothic, plants were, for the most part, be divided into those regenerating health (short "hp reg") and those regenerating mana (short "mana reg"). Following this categorization we can list them as follows:

## HP Reg Plants

| DE | Internal | Effect | Note |
|----|----------|--------|------|
| Waldbeere | woodberry | +10 HP |   |
| Flammendorn | flameberry | +12 HP |
| Seraphis | seraphis | +14 HP | |
| Velayis | velayis | +16 HP | unused |
| Bergmoos | mountain moss | +18 HP | |
| Grabmoos | gravemoss | +20 HP | |
| Nachtschatten | nightshadow | +22 HP | |
| Mondschatten | nightshadow_02 | +24 HP | |
| Orkblatt | orcherb_01 | +26 HP | |
| Eichenblatt | orcherb_02 | +28 HP | |
| Heilkräuter 1 | | +30 HP | |
| Heilkräuter 2 | | +39 HP | |
| Heilkräuter 3 | | +49 HP | |

All of these plants only impacted HP and had no other effects. From the woodberry to the healing herb they all gave progressively more HP bonus in steps of +2, until bigger jumps in case of the last two healing herbs. These 13 plants can be divided into 6 categories: 
1. Berries (to which also a third berry counts, the Trollkirsche (Troll Cherry), which is poisonous and gives -20 HP, unused like Velayis). 
2. Velayis + Seraphis (perhaps "flowers".
3. Moss
4. Nightshade Plants
5. "Leaves"
6. Healing Herbs

...

## Mana Reg Plants

| DE | Internal | Effect | Note |
|----|----------|--------|------|
| Blutbuchensamen | | +5 Mana |   |
| Turmeichensamen | | +10 Mana |
| Rabenkraut | | +15 HP | |
| Dunkelkraut | | +20 Mana | |
| Steinwurzel | | +25 Nana | |
| Drachenwurzel | | +30 Mana | |

The same principle as above, but only 6 instead of 13 plants and 3 instead of 6 categories:
1. (Mana) Seeds
2. (Mana) Herbs
3. (Mana) Roots

## Sequel Plants

In the Sequel documentation on plants and alchemy by Nyul and Filler, a few of those plants were not mentioned, while apparently three additional ones were added. 

Not mentioned were the following:
* Seraphis/Velayis
* Grabmoos (?)
* Eichenblatt
* Sklavenbrot
* Blutbuchensamen/Turmeichensamen
* Dunkelkraut
* Drachenwurzwl

And these have been added:
* Blutdistel (Blood Thistle)
* Silberfarn (Silver Fern)
* Königstrost (-)
* Blutfarn (also mentioned somewhere in the scripts?)

While Seraphis as a name did no longer appear, the Blood Thistle used Seraphis' old model and texture. It could well be that some plants weren't removed or replaced, but rather renamed. If so, Seraphis could be the scientific term (as used by Alchemists), while blood thistle would be the more common name. The visuals should not be considered to be final either. 

Some plants were meant to have a different effect in the Sequel: 
* ...


### Naming Convention

In the item scripts of Gothic there is an extra file (plants.d) reserved for plants, but it was left empty. Instead all plant IDs were written into the food file and named `ItFo_Plant_[Name]`. It makes sense insofar as that the plants have been an afterthought and couldn't be properly implemented into an alchemy crafting mechanic as they planned; they therefore served no other purpose anymore but as food. The Sequel wanted to correct this shortcoming. Consequentally the plants scripts were moved and a new naming convention was introduced, which we'll follow: `ItPl_[Name]`. 

