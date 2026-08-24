# Plants & Mushrooms

Author: *flosha*, add date from old docs  
Last update: 20.08.2026


In Gothic, plants were, for the most part, divided into those regenerating health (short "hp reg") and those regenerating mana (short "mana reg"). Following this categorization we can list them as follows (internally, they followed the scheme `ItFo_Plants_[ID]`; for simplcities sake we ommit the prefixes and only list the IDs below): 

## HP Reg Plants

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


## Mana Reg Plants

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

| DE       | Internal | Effect | Note |
|----------|----------|--------|------|
| Waldpilz | ItMu_WoodMushroom | ? | Phoenix addition, based on the Comic |
| Waldpilz 2 | ItMu_WoodMushroom_02 | ? | 
| Honigpilz | ItMu_HoneyMushroom | ? | Alpha, especially rare wood mushroom |
| Höhlenpilz | ItMu_CaveMushroom | ? | Alpha/Sequel, more common cave mushroom |
| Sklavenbrot | ItMu_CaveMushroom_02 | ? | | 
| Erzpilz | ItMu_OreMushroom | ? | Poisonous Cave mushroom, Phoenix addition, based on the Comic |
| Teufelspilz | ItMu_DevilsMushroom | ? | very rare mushroom, poisonous by touch |

mushroom_01
mushroom_02


## Sequel Plants

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
* Blutfarn (also mentioned somewhere in the scripts?)

While Seraphis as a name did no longer appear, the Blood Thistle used Seraphis' and Velayis' old model and texture. It could well be that some plants weren't removed or replaced, but rather renamed. If so, Seraphis or Velayis could be the scientific term (as used by Alchemists), while blood thistle would be the more common name. The visuals should not be considered to be final either. 

While there does not seem to be a real blood thistle - regular thistles very much have the color Seraphis comes with; we would only have to regard the purple berry texture that the middle part uses as a placeholder for a thistle blossom. If we would follow the example of Silverfern and Bloodfern, there could as well be a silver thistle (which actually exists) and a blood thistle, which would be the more rare variant.  

Some plants were meant to have a different effect in the Sequel: 
* ...


## Plant Distribution

As a matter of fact the game world of Gothic has been still almost completely empty (no items being distributed) in versions as late as v0.94. Plant items included. All of the plants items were added a few weeks before release in a hurry, as so many other things. Due to this the plants have been distributed randomly without following any rules. 

It was done so randomly and under so much time pressure, that the cave mushroom (Höhlenpilz) got renamed into hell mushroom (Höllenpilz) in order to "fix" the mistake of a level designer who had put it all over the surface in open light, instead of in caves and other dark places only. There simply was no time left to do things properly. 

The team behind the Gothic Sequel, Nyul and Filler in particular, wanted to fix all of these mistakes. They renamed the mushroom into Cave Mushroom again and started writing a small plant documentation with guidelines for plant distribution. They summarised their plans as follows (from the `Sequel Design Documentation`):  

> Die Pflanzen sollen nicht "wie in Gothic" mal hier und dort mitten auf dem Weg kreuz und quer durcheinander verteilt werden, sondern aufgrund dieser Verteilungsliste in bestimmten Gebieten in kleinen Gruppen verteilt werden.

> EN: Plants shouldn't "like in Gothic" be distributed messily here and there in the middle of the road, but they should be distributed based on this distribution list in particular small groups. 
  
> Locations nutzen die neben den Wegen liegen! Es gibt unglaublich viele Locations die der Spieler durch herumlaufen/klettern erreichen kann, die in GOTHIC leer waren. Der Spieler soll durch das Erreichen/entdecken  dieser Locations mit ein paar Pflanzen belohnt werden.		

> Use locations that are on the side of the road! There are unbelievably many locations that the player can reach by running around or climbing, which were empty in GOTHIC. The player should be rewarded by reaching/discovering these locations. 

> Das bedeutet allerdings nicht, das der Spieler "on_the_fly" nicht ein paar Pflanzen einsacken kann, weil er nur auf dem Weg läuft. Auch hier wird er fündig, aber das Gro der Pflanzen will gefunden werden! Pflanzen wachsen in Gruppen :) zu (mind)zwei - X(max) zusammen. (Inflation bedenken! Findet der Spieler 20 wertvolle Pflanzen an einer Location ist er reich!	

> This does not mean though, that the player cannot loot some plants "on_the_fly", as he only walks on the road. Here too he will find something, but the majority of plants wants to be found! Plants grow in groups :) at a minimum of two to X (max) together. (Consider inflation! If the player finds 20 valuable plants at one location he is rich!)

> Verteilungsrichtlinie: Je wertvoller die Pflanze desto weniger gibt es davon und desto versteckter ist die Pflanze.		

> Guiding Principle: The more valuable the plant, the less of it there is and the more hidden is the plant. 

Todo: Add distribution list with distribution guidelines for each camp. 


## Naming Convention

In the item scripts of Gothic there is an extra file (plants.d) reserved for plants, but it was left empty. Instead all plant IDs were written into the food file and named `ItFo_Plant_[ID]`. It makes sense insofar as that the plants have been an afterthought and couldn't be properly implemented into an alchemy crafting mechanic as they planned; they therefore served no other purpose anymore but as food. The Sequel wanted to correct this shortcoming. Consequentally the plants scripts were moved and a new naming convention was introduced, which we'll follow: `ItPl_[ID]`.  
For Mushrooms we are using `ItMu_[ID]`. Since they even have an associated alpha talent (`Identify_Mushrooms`) and as there will be much more mushrooms than the two remaining in the release version, they are in a script file on their own (mushrooms.d).  


---


## Phoenix Plants & Mushrooms

| DE          | Internal             | Effect | Note         |
|-------------|----------------------|--------|--------------|
| Waldpilz    | ItMu_WoodMushroom    | ?      | Comic        |
| Waldpilz 2  | ItMu_WoodMushroom_02 | ?      |              |
| Honigpilz   | ItMu_HoneyMushroom   | ?      | Alpha        |
| Höhlenpilz  | ItMu_CaveMushroom    | ?      | Alpha/Sequel |
| Sklavenbrot | ItMu_CaveMushroom_02 | ?      |              | 
| Erzpilz     | ItMu_OreMushroom     | ?      | Comic        | Poisonous Cave mushroom, Phoenix addition, based on the Comic |
| Teufelspilz | ItMu_DevilsMushroom  | ?      | Alpha        | very rare mushroom, poisonous by touch |




## Plants as alchemical ingrediences

There are potions with temporary and potions with permanent effect. Temporary potions require *Alcohol* as their resolvent, permanent potions require *Quicksilver*. 

---

ToDo: Change Effect values to fit to the Alpha attribute values. 

---

Balancing:  
Due to the alpha attribute values, the potion values had to be heavily modified to fit into this scheme. 
When there is a maximum of 15 Strength, 30 HP, 30 Psi, 30 Mana etc., perm potions cannot give boni as high as they did in the release version (e.g. +5, +10, +15) where one could acquire three or more times as much points.  
We follow the simple scheme of "light", "medium" and "heavy" potions:
* Essences: Light Perm Potions: +1
* Extracts: Medium Perm Potions: +2
* Elixiers: Heavy Perm Potions +3

Since we have to restrict the boni of potions as much, the rare plants required for these potions won't give any perm values on their own. They have to be used for potions in order to make full use of them. 

The player can buy potions, he can craft potions himself (if he has the necessary alchemical knowledge) or (if he hasn't) he can ask and pay alchemists to do it for him (if he knows any who are capable and willing to help him).  


### Etymology and Meaning

Gothic divided potions into "Essences", "Extracts" and "Elixirs", regarding each of those to be a stronger "extraction" than the former, therefore having a stronger effect.  

Each potion requires a "resolvent" ("Lösungsmittel"). Potions of temporary effect require Alcohol as their resolvent, following the Sequel design (more precisely "rectified spirit", in German we use the term "Weingeist" as it has been utilised for alchemical purposes in medieval times). In Phoenix, the potions of permanent effect require the much more costly Quicksilver as their resolvent, by which we incorporate another unused alchemical item. 
Lore-wise, the spirit is made in the backrooms of Silas bar and also bought by the mages of the fire circle for their alchemical purposes. Kalom may or may not make it himself.  
Todo: How is quicksilver made or where does it come from? Bought from the Outside World? 

When we design alchemy as a crafting mechanic, as they have planned, the meaning of those terms should be clarified, since teachers have to explain them ingame and it will have to influence how the respective potions are made. 

**Extracts or "Tinctures"**: When plants are soaked in alcohol to slowly give (solve) their extract into the resolvent, the result is called a tincture. This term is not used in the game yet. 
* It should be done in a ratio of about 1:5 to 1:10 between plant and resolvent (e.g. 100g of the plant, 1 liter Alcohol).
* It can be done with fresh plants (resulting in weaker tinctures) or with dried, pulverized plants (resulting in stronger tinctures, about twice as strong).
* A tincture is always an "extract", but an "extract" is not always a tincture. The difference is that there are dry and liquid extracts and tinctures are liquid extracts. This means, that all extracts in the game, being liquid, are tinctures.

* **Essences**: What is the difference between an extract or tincture and an essence? In the alchemical context, essences are to be seen as weaker in (physical) effect than extracts, but are more complex to make and may be speculated to be higher in effect in other, more subtle and spiritual ways. From a materialist perspective an extract contains more than an essence, more measurable concentrated material, while from an alchemical perspective the essence may be considered to be of higher quality and effect.
* This leads to some conflict with the game, where the essence is clearly considered to be the weaker of the two. A way to dissolve this conflict, may be: An essence contains (materially) less, but exactly for this reason it may be necessary, since an extract may be too strong to handle (e.g. for the initiant mage), and to create such an essence, which will alter the mage in substantial, spiritual ways (e.g. making him receptable for the mana in the first place), more skill may be required. In this way, essences can remain the theoretically weaker potion in the game, but require higher skill to make. Potentially the highest. For non-alchemists it may be relatively easy to create mana extracts, but they will always be poisonous. Only if the initiant has been prepared through an essence can one handle the consumption of materially stronger extracts. 

**Elixirs**: 
...  













