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


**Mushrooms:**  

| DE | Internal | Effect | Note |
|----|----------|--------|------|
| Waldpilz | ItMu_WoodMushroom | ? | Phoenix addition, based on the Comic |
| Waldpilz 2 | ItMu_WoodMushroom_02 | ? | 
| Honigpilz | ItMu_HoneyMushroom | ? | Alpha, especially rare wood mushroom |
Phoenix addition, based on the Comic |
| Höhlenpilz | ItMu_CaveMushroom | ? | Alpha/Sequel, more common cave mushroom |
| Sklavenbrot | ItMu_CaveMushroom_02 | ? | | 
| Erzpilz | ItMu_OreMushroom | ? | Poisonous Cave mushroom |
| Teufelspilz | ItMu_DevilsMushroom | ? | very rare mushroom, poisonous by touch |

All of these plants only impacted HP and had no other effects. From the woodberry to the healing herb they all gave progressively more HP bonus in steps of +2, until bigger jumps in case of the last two healing herbs. These 13 plants can be divided into 6 categories: 
1. Berries (to which also a third berry counts, the Trollkirsche (Troll Cherry), which is poisonous and gives -20 HP, unused like Velayis). 
2. Velayis + Seraphis (perhaps "flowers".
3. Moss
4. Nightshade Plants
5. "Leaves"
6. Healing Herbs
7. Mushrooms

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


### Temp Potions

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


### Perm Potions

| Potion | Ingrediences | Effect |
|--------|--------------|--------|
| HP Perm. 1 | 1 Quecksilber, 1 Grabmoos, 1 Velayis, 1 Nachtschatten | +5 Leben |
| HP Perm. 2 | 1 Quecksilber, 1 Grabmoos, 2 Velayis, 2 Nachtschatten | +10 HP |
| HP perm. 3 | 1 Quecksilber, 1 Grabmoos, 3 Velayis, 3 Nachtschatten | +15 HP |
Mana Perm. 1 | 1 Quecksilber, 1x Erzpulver, 1 Drachenwurzel, 1 Dunkelkraut, 1 Nachts. | +5 Mana |
Mana Perm. 2 | 1 Quecksilber, 2x Erzpulver, 2 Drachenwurzel, 2 Dunkelkraut, 2 Nachts. | +10 Mana |
Mana Perm. 3 | 1 Quecksilber, 3x Erzpulver, 3 Drachenwurzel, 3 Dunkelkraut, 3 Nachts. | +15 Mana |
Const. Perm 1	| 1 Quecksilber, 1 Königstrost, 1 Honigpilz, 1 Nachts. | +5 Const. |
Const. Perm 2 |	1 Quecksilber, 2 Königstrost, 2 Honigpilz, 2 Nachts. | +10 Const. |
Const. Perm 3 |	1 Quecksilber, 3 Königstrost, 3 Honigpilz, 3 Nachts. | +15 Const. |
Psi Perm. 1 | 1 Quecksilber, 1x Psi-Wurzel, 5x Crawlersekret, 1 Sumpfkraut, 1 Nachts. | +5 Will	|
Psi Perm. 2	| 1 Quecksilber, 1x Psi-Wurzel, 10x Crawlersekret, 2 Sumpfkraut, 1x 2 Nachts. | +10 Will |
Psi Perm. 3	| 1 Quecksilber, 1x Psi-Wurzel, 20 Crawlerzangen, 3 Sumpfkraut, 3 Nachts. | +15 Will |
Str perm.	1	| 1 Quecksilber, 1 Eichenblatt, 1 Sklavenbrot, 1 Nachts. | +2 Str |
Str. perm. 2 | 1 Quecksilber, 2 Eichenblatt, 2 Sklavenbrot, 2 Nachts. | +4 Str |
Str. perm. 3 | 1 Quecksilber, 3 Eichenblatt, 3 Sklavenbrot, 3 Nachts. | +8 Str |
Dex Perm | 1 Quecksilber, 1 Blutfarn, 1 Honig, 1 Nachtschatten |	+2 Dex |
Dex Potion 2 | 1 Quecksilber, 2 Blutfarn, 2 Honig, 2 Nachtschatten	| +4 Dex |
Dex Potion 3 | 1 Quecksilber, 3 Blutfarn, 3 Honig, 3 Nachtschatten	| +8 Dex |
Special Potion 1 | 1 Quecksilber, 1 Eichenblatt, 1 Mondschatten | +4 Str/Dex |
Special Potion 2 | 1 Quecksilber, 2 Eichenblatt, 2 Mondschatten | +6 Str/Dex	|

Balancing:  
Due to the alpha attribute values, the potion values have to be heavily modified to fit into this scheme. 
When there is a maximum of 15 Strength, 30 HP, 30 Psi, 30 Mana etc., perm potions cannot give boni as high as they did in the release version where one could acquire three or more times as much points.  
We follow the simple scheme of "light", "medium" and "heavy" potions:
* Essences: Light Perm Potions: +1
* Extracts: Medium Perm Potions: +2
* Elixiers: Heavy Perm Potions +3

Since we have to restrict the boni of potions as much, the rare plants required for these potions won't give any perm values on their own. They have to be used for potions in order to make full use of them. 

The player can buy potions, he can craft potions himself (if he he has the necessary alchemical knowledge; or, if he hasn't,) he can ask and pay alchemists to do it for him (if he knows any who is capable and willing to help him).  


### Etymology and Meaning

Gothic divided potions into "Essences", "Extracts" and "Elixirs", regarding each of those to be a stronger "extractions" than the former, therefore having a stronger effect.  

Each potion requires a "resolvent" (Lösungsmittel). In Phoenix, potions of temporary effect require Alcohol ("rectified spirit", in German we use the term "Weingeist" as it has been used for potions in medieval times) as their resolvent, following the Sequel design, while potions of permanent effect require the much more costly Quicksilver as their resolvent, by which we incorporate another unused alchemical item. Lore-wise, the spirit is made in the backrooms of Silas bar and also bought by the mages of the fire circle for their alchemical purposes. Kalom may or may not make it himself. 

When we design alchemy as a crafting mechanic, as they have planned, the meaning of those terms should be clarified, since teachers have to explain them ingame and it will have to influence how the respective potions are made. 

**Extracts or "Tinctures"**: When plants are soaked in alcohol to slowly give (solve) their essence into the resolvent, the result is called a tincture. This term is not used in the game yet. 
* It should be done in a ratio of about 1:10 between plant and resolvent (e.g. 100g of the plant, 1 liter Alcohol).
* It can be done with fresh plants (resulting in weaker tinctures) or with dried, pulverized plants (resulting in stronger tinctures, about twice as strong).
* A tincture is always an "extract", but an "extract" is not always a tincture. The difference is that there are dry and liquid extracts and tinctures are liquid extracts. This means, that all extracts in the game, being liquid, are tinctures.

* **Essences**: What is the difference between an extract or tincture and an essence? In the alchemical context, essences are to be seen as weaker in (physical) effect than extracts, but are more complex to make and may be speculated to be higher in effect in other, more subtle and spiritual ways. From a materialist perspective an extract contains more than an essence, more measurable concentrated material, while from an alchemical perspective the essence may be considered to be of higher quality and effect.
* This leads to some conflict with the game, where the essence is clearly considered to be the weaker of the two. A way to dissolve this conflict, may be: An essence contains (materially) less, but exactly for this reason it may be necessary, since an extract may be too strong to handle (e.g. for the initiant mage), and to create such an essence, which will alter the mage in substantial, spiritual ways, e.g. making him receptable for the mana in general, more skill may be required. In this way, essences can remain the theoretically weaker potion in the game, but require higher skill to make. Potentially the highest. For non-alchemists it may be relatively easy to create mana extracts, but they will always be poisonous. Only if prepared through an essence can one handle the consumption of materially stronger extracts. 

**Elixirs**: 












