# Plants & Alchemy

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

---

## Plants as alchemical ingrediences

There are potions with temporary and potions with permanent effect. Temporary potions require *Alcohol* as their (Lösungsmittel?), permanent potions require *Quicksilver*. 

| Potion | Ingrediences | Effect |
|--------|--------------|--------|
| Essenz der Heilung	| 1 Alkohol, 1 Bergmoos, 1 Waldbeere | 25 HP |
| Extrakt der Heilung | 1 Alkohol, 1 Bergmoos, 2 Waldbeere | 50 HP |
| Elixier der Heilung | 1 Alkohol, 1 Bergmoos, 3 Waldbeere | 100 HP |
| Mana Essenz |	1 Alkohol, 1 Steinwurzel, 1 Rabenkraut | 25 Mana |
| Mana Extrakt | 1 Alkohol, 1 Steinwurzel, 2 Rabenkraut | 45 Mana |
| Mana Elixier | 1 Alkohol, 1 Steinwurzel, 3 Rabenkraut | 65 Mana |
| Essenz der Ausdauer	| 1 Alkohol, 1 Blutdistel, 1 Honig	|	1 Min |
| Extrakt der Ausdauer | 1 Alkohol, 2 Blutdistel, 2 Honig	|	2 Min |
| Elixier der Ausdauer | 1 Alkohol, 1 Blutdistel, 3 Honig |	3 Min |
| Psi Essenz | 1 Alkohol, 1x Crawlersekret, 1x Sumpfkraut | 25 Psi |
| Psi Extrakt | 1 Alkohol, 1x Crawlersekret, 2x Sumpfkraut | 45 Psi |
| Psi Elixier | 1 Alkohol, 1x Crawlersekret, 3x Sumpfkraut | 65 Psi |

ToDo: Change Effect values to fit to the Alpha attribute values. 
