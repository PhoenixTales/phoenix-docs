# Attributes 

<span class="changed">[WORK IN PROGRESS!]</span>

![Attributes](/_img/headings/attributes.png)

```
Author: Flosha 
Status: <span class="changed">Work in progress</span>

Written:    30.12.18 - 27.12.20
Rewritten:  03.11.22 - 04.12.22
```

At first we analyse the attributes as imagined in the concept phase by analysing all the available design documents. Then we look at the attributes as they were implemented in the actual builds of the game and how they changed in course of development. In the end, building on this research, we present our own solution for **Phoenix**. 


## Alpha Attributes

Based on the high number of items we assume that the very first list of attributes, that Mike put together in his handwritten notes, is to be found among his ideas on spells (p.8 of the spells.pdf where we have published all of Mikes spells notes combined). It is the oldest mentioning of attributes we know of and perhaps the oldest source there is.  

Mike wrote down the abbreviations on the left *only*; the meaning on the right is based on our research. The list is not really to be seen as a specific plan to implement the attributes as such, but more as a list of potential attributes that may or may not be useable for the game to be made.  

```
Note:      Meaning:
ST         ST  = Stärke (Strength)
KON        KON = Konstitution (Constitution)
We         We  = Weisheit (Wisdom)
DK         DK  = Diebeskunst (Thievery)
WK         WK  = Waffenkunst (Weaponry)
SK         SK  = Schießkunst (Marksmanship)
AG         AG  = Arkane Gabe (Arcane Gift)
WIL        WIL = Wille (Will)
CH         CH  = Charisma (Charism)
Wa         Wa  = Wahnsinn (Madness)
```

The meaning of most of these abbreviations is clear and can be confirmed by comparison with the same terms used at other places as we will show below.  

"We" as *Weisheit* (Wisdom) and "Wa" as *Wahnsinn* (Madness) remain speculative but likely. SK on the other hand was hard to make sense of. We thought of *Schnelligkeit* (speed), *Sprachkunst* (philology) and *Streitkunst* (disputation). They all seemed unlikely for different reasons.  
Then I had the idea of it refering to *Schwarze Kunst* ("Black Art"), in the sense of the *Dark Arts* (a term as it is used in the description of the robe of Xardas (*Robe der Dunklen Künste*  = Robe of the Dark Arts), that refers to such things as necromancy and invocation. Shortly after, Wunddorn came up with the idea of *Schießkunst* (marksmanship) and although I am fond of my *Dark Arts* idea, Marksmanship seems most likely to be the meaning of SK. 

Note that there is no mentioning of healthpoints or mana in the list.  


### Primary & Secondary Attributes

We've got two more handwritten lists of attributes (both to be found next to each other in `Orpheus B-Scribbles`, p. 8) with a few differences. We assume that these lists originated shortly after the first list mentioned above. They also consist of abbreviations only without any explanation.

```

                           STR   TP
                        ---------------
                           WK
    STR  -  CON            DK
    KaGe    AT          ---------------
    DiGE    GE             CON  LP
    AGa     MANA           AGa  MANA
    WIL     WIL            WIL  WS

```

What this initial structure suggests is a correlation of the attributes as they are listed here on the two columns of each table.  

The first table points at a correlation between Strength (`STR`) and Constitution (`CON`), the second at a correlation between Strength and Hitpoints (`TP`, *Trefferpunkte*, which in this context should be the damage points you deal), while Constitution is here related to Healthpoints (`LP`, *Lebenspunkte*, refering to the hitpoints of your character; the damage you can endure).  

Arcane Gift (`AGa`, *Arkane Gabe*) is correlated to Mana. Will (`WIL`, *Wille*, the psi-energy) is at first correlated to an identical attribute name, then to "WS" (which may either stand for *Willensstärke* (Willpower) or *Wahnsinn* (Madness); both terms were used inside the game at different points.  
This search for a name and differentiation between Psi/Will, Willpower, Madness and Sanity continues during development and will also be seen inside the builds we will analyse further below.  

The abbreviations `KaGe` and `DiGe` have to stand for *Kampfgeschick* ("combat skill") and *Diebesgeschick* ("thief skill") respectively. Otherwise they were named `WK` (*Waffenkunst* = Weaponry, which in the builds was called `Swordsmanship`) and `DK` (*Diebeskunst* = Thievery). While on the second table they were not put into correlation with another attribute, in the first one they were. Thievery was most likely associated with Dexterity (`GE` = *Geschicklichkeit*) and Weaponry with `AT`, which, as far as we know, simply stands for Attack.  

Mike also considered endurance/stamina (German: Ausdauer) as a potential factor on the same page, but discarded it immediately:

> ~~AUSDAUER?~~
> NO

From the first list that we think of as the original pool of attribute ideas a few were already discarded, such as We (that we assume to be Wisdom), SK (assumed to be Marksmanship) and CH (assumed to be Charisma), while Wa (assumed to be Madness) was put into "second order". The rest remained.  

This structure remained almost unchanged for a long time in development. The same six attributes as seen on the two tables above appear in a later (typed) document by Mike (`Phoenix_B4_Learning.doc`, p. 4), changed last at 06.07.99, now with the full meaning given:

```
+--------------+--------------+
| Attribute    | Attributes   |    
|--------------+--------------|  
| Stärke       | Strength     |  
| Konstitution | Constitution |
| Diebeskunst  | Thievery     |
| Waffenkunst  | Weaponry     |
| Arkane Gabe  | Arcane Gift  |
| Wille        | Will         |
+--------------+--------------+
```

While in a document written by Alex Brüggemann (`Phoenix_B1_AttributesTalentsActions.doc`), changed last at 21.07.99, only five attributes were listed. Constitution, Thievery, Weaponry and Arcane Gift are not mentioned at all.   

```
+-------------+----------------+
| Attribute   | Attributes     |
|-------------+----------------|
| Stärke      | Strength       |
| Geschick    | Dexterity      |
| Mana        | Mana           |
| PSI-Energie | Will(power)    |
| Leben       | Health         |
+-------------+----------------+
```

To add additional confusion, both the five and the six attributes can also be found in v0.56c-0.64b simultaneously. While the `constants.d` in both versions lists the six attributes mentioned by Mike, the `text.d` followed the list of five.  

Somewhere between v0.64b (07.1999) and v0.94k (10.2000), the `constants.d` was adjusted to the five attributes as they were structured in the `text.d` since at least v0.56c. So while they did co-exist for quite some time and were in some way associated with each other, at some later point it was decided - for unknown reasons - to remove the original attributes. 

Gladly in the before-mentioned doc (`Phoenix_B4_Learning.doc`, p. 5) by Mike there is a little note with an explanation that is able to dissolve the confusion:  

> **Progression of maximal status attributes**  
> When the player increases Constitution, his LP<sub>max</sub> are increased too, the same with Arcane Gift -> MP<sub>max</sub> and Will -> WP<sub>max</sub>. When this occurs, a slow increase in length of the bar maximum can be seen inside the status screen, which displays the increasing status attribute as a (more or less filled) bar.  

Based on these findings we can conclude that the original idea by Mike - persisting for at least two years in development - was to have the six primary attributes listed above which names were supposed to be refered to inside of the game and that were responsible to scale the secondary "status attributes", which most likely were not supposed to be refered to inside of the game and instead should have appeared *only* in form of symbols or bars in the user interface.  


### Attribute levels in text form

This analysis is additionally confirmed by the so called "clear texts for attributes" in the `text.d` of v0.56c which may be a remnant of even earlier versions. Only the six attributes are described here in clear text for every attribute level, while there is none for the five "second order" attributes. We won't quote all those clear texts here, as they were highly work in progress and many were lacking, but they should have been structured in the following way, with ten possible levels for each of the attributes:  

```
// Klartexte für Attribute ( Konzept 1.3.2 )
```

```
CONST STRING TXT_ATR_HP [MAX_TXT_ATR] = {
	"Unbrauchbar",
	"Miserabel",
	"Sehr schlecht",
	"Schlecht",
	"Mäßig",
	"Normal",
	"Gut",
	"Sehr gut",
	"Hervorragend",
	"Exzellent"
```

You may notice that there are *seven* attributes in the ``text.d``, the six primary attributes and `ATR_HP`, as seen above. But these "HP" are not to be confused with the `ATR_HITPOINTS` of NPCs. They're described as *Strukturpunkte* (structure points) in the associated comment and as such they are the hitpoints of *items*, which is also confirmed by the wording above (such as "unbrauchbar" (= unuseable), refering to the condition of a broken item).  

It is safe to assume that NPCs should have referred to the first order attributes inside of the game using such descriptive words as a feedback for the player; for his character progression, for the condition of items in trading and so forth. I call this *Immersion durch Verbalisierung* (= immersion by verbalisation).  
They would talk about the strength and constitution, the arcane gift, the weapon and thief skills and the will/madness of the player and other characters, while not refering to the more abstract and internal *points* in form of the correlated, secondary or deduced attributes: Hitpoints, Willpoints and Manapoints.  

Some of the first order attributes are still mentioned in the release version of the game, such as Arcane in form of the ingame book *Elementare Arcanei* and in *Machtvolle Kunst*, which is introduced as: *Ein Werk für den Eingeweihten der Arkanen Kunst* (= A work for the Initiated of the Arcane Art).  

If the first order attributes were ever supposed to appear in the character profile they would have appeared in the described text form per level; while the second order attributes wouldn't have been mentioned ingame at all and would only be displayed in the interface by the associated symbols or bars.  

<p class="subtext">But not all the bars on the HUD were direct representations of the status attributes. For instance in later versions there is a bar representing the oxygen when being underwater. This is not linked to an attribute but controlled by a guild value in the species script, as Auronen pointed out. There is a `SWIM_TIME` and a `DIVE_TIME` defining the swim/dive endurance before receiving damage.  

While Mike discarded the idea of endurance as an attribute on its own, there was obviously a need to restrict the dive time. In the same way we can imagine that you were not supposed to be able to sprint infinitally. But instead of restricting the feature (by something like Endurance or a value like `SPRINT_TIME` they removed the sprinting on key press and linked it to speed potions.
</p>


### Attribute Progression

Mike refered to the primary attributes just as "the six attributes" or as "character values". In `Phoenix_B4_Learning.doc` he explains that these six attributes can be learned/increased from teachers just as talents and spells. Upon increase of one of the six primary attributes, the associated secondary attributes (that Mike refers to as "status attributes") are increased alongside.  

In `Phoenix_B1_AttributesTalentsActions`, Alex describes the maximum values of the status attributes in the symbol HUD that was used (or planned) at this point: 

```
+-------------+-------------+------------+
| Attribute   | Start-Value | Max-Value  |
|-------------+-------------+------------|
| Strength    | 3 Symbols   | 10 Symbols |
| Dexterity   | 3 Symbols   | 10 Symbols |
| Mana        | -           | 10 Symbols |
| PSI-Energy  | -           | 10 Symbols |
| Health      | 5 Symbols   | 20 Symbols |
+-------------+-------------+------------+
```

But in `Phoenix_C2_Monsters` and almost in the same way in the remnants of a later version of the Phoenix Concept, which were also written by Alex, they are structured like this (RS stands for Resistance):  

```
+------+------+------------+------+-----------+------------+
| LE   | RS   | STR        | DEX  | MAN       | WIL        |
|------+------+------------+------+-----------+------------|
| 5-20 | 0-10 | 1-10 (15?) | 1-10 | 1-10 (15) | 1-10 (15?) |
+------+------+------------+------+-----------+------------+
```

Accordingly in v0.56c-0.64b the NPCs have at most 20 HP, 10 Str (with one exception of 30, which we assume to be a mistake), 10 Dex, but the maximum Mana and Madness value have been increased to 20. Even in v0.94k the character value progression was still basically following this old structure but now with a maximum Health, Will and Mana of human NPCs of 30, while the maximum Strength and Dexterity was 15.  

In course of this research we discovered and summarised some defaults.  


### Default Attribute Values for NPCs

0.94k is the most valuable source to analyse the values of the different guilds and ranks of NPCs. Although values vary for individual NPCs with their unique traits, we could identify a consistent set of light, medium and heavy default values:  

```
Workers (VLK, SFB, BAU, NOV):
L: 10 Hp, 5 Str, 5 Dex. 0 Mana, 0 Will (NOV 10 Will)
M: 14 Hp, 7 Str, 6 Dex, 0 Mana, 0 Will (NOV 10 Will, 5 Str) 
H: 18 Hp, 9 Str, 7 Dex, 0 Mana, 0 Will (NOV 10 Will, 5 Str)

Warriors (GRD, SLD, TPL & EBR=E):
L: 18 Hp,  9 Str,  7 Dex, 0 Mana, 0 Will  (TPL 10 Will)
M: 22 Hp, 11 Str,  8 Dex, 0 Mana, 0 Will  (TPL 10 Will)
H: 26 Hp, 13 Str,  9 Dex, 0 Mana, 0 Will  (TPL 10 Will)
E: 30 Hp, 15 Str, 10 Dex, 0 Mana, 0 Will

Thieves (STT, ORG):
L: 18 Hp, 7 Str,  9 Dex, 0 Mana, 0 Will
M: 22 Hp, 8 Str, 11 Dex, 0 Mana, 0 Will
H: 26 Hp, 9 Str, 13 Dex, 0 Mana, 0 Will

Mages (KDF, KDW):   
*: 30 Hp, 5 Str, 10 Dex, 30 Mana, 0 Will

Gurus (GUR):
*: 30 Hp, 5 Str, 10 Dex, 0 Mana, 30 Will
```

In some cases (as with the Barons, Mages and Gurus) NPCs shared the same values and it is likely that they should have been differentiated more. These values are what we would describe as the intended default values for "Archmages" (such as Corristo, Saturas), Warrior-Leaders (such as Gomez, Lee and Angar), the Enlightened (Y'Berion) and Master-Thieves (such as Lares); but more on that in the section on attributes in Phoenix.  

Default attributes for Monsters were a bit different. Monsters had up to 50 HP, Strength and Dex. In 0.94k, most monsters didn't have any Will or Mana Attribute associated with them (anymore), with the exception of the Wolf with 2 Mana and 2 Will. In the Gothic Gameplay Trailer from 2000 you see this system in action where the Troll has 30 HP, as Dmitriy pointed out; the Demon seems to have 30 Str.  


### Attributes & Classes

We should also indicate that the initial attributes seem to have been envisioned with the four classes in mind. We can assume that they would have been heavily correlated with the class specific character progression; in which way remains speculative.  

* **General:** Strength / Constitution
	* Strength -> Damage
	* Constitution -> Health
* **Warrior:** Weaponry -> Attack 
* **Thief:** Thievery -> Dexterity
* **Mage:** Arcane Gift -> Mana
* **Psionic:** Will -> Madness


### Cut Attributes

```
ATR_ARCANE ATR_CONSTITUTION ATR_DEXTERITY ATR_HITPOINTS ATR_HITPOINTS_MAX ATR_MADNESS ATR_MADNESS_MAX ATR_MANA ATR_MANA_MAX ATR_PROTECTION ATR_REGENERATEHP ATR_REGENERATEMANA ATR_RESIST_FIRE ATR_RESIST_MAGIC ATR_RESIST_POISON ATR_RESIST_WEAPON ATR_STRENGTH ATR_SWORDSMANSHIP ATR_THIEVERY ATR_INDEX_MAX
```

Above is a list of all the technical `ATR` constants in the engine from the `Worldfile.txt` to be found in the Gothic-MDK. As you see, what we analysed before as first and second order attributes and what the developers clearly differentiated in their design concept was all mixed up in the constants. Not only was there no differentiation between first and second order attributes but there were also so called "zusätzlich als Attribut geführte Werte" (= "values which are additionally handled as attributes"), constants which were not *really* supposed to be attributes but were handled as such for technical reasons.  

Such is the case for `ATR_PROTECTION`, which was later replaced by a dedicated `PROT_*` constant for the different forms of protection, such is also the case for ``ATR_RESIST_*`` and finally for the later introduced `ATR_REGENERATEHP` and `ATR_REGENERATEMANA`; both of which were not planned to be listed among the actual attributes, both of which remained unused in the release and both of which would have worked just as well with a dedicated constant.  

In the `text.d` of v0.56c there is another case like that in form of "*Tarnung*" (disguise), which had no equivalent (anymore or not yet?) among the constants, but just as protection it was not really supposed to be an attribute.  

<p class="subtext">In 0.56c-0.64b the maximum attribute index was 18. In 0.94k it was 10. In 1.00b onwards it was 8.</p>

When we blend out these attributes that were only handled as such for technical reasons (usually just tempory), we end up with the following comparison of attribute constants throughout the available builds, as they were continueously reduced:  

```
+----+-------------------+--------------------+--------------------+
|    | 0.56c/0.64b       | 0.94k              | 1.00b - 1.12f      |
|  - | ----------------- | ------------------ | ------------------ |
|  0 | ATR_HITPOINTS	 | ATR_HITPOINTS      | ATR_HITPOINTS      |   
|  1 | ATR_HITPOINTS_MAX | ATR_HITPOINTS_MAX  | ATR_HITPOINTS_MAX  |
|  2 | ATR_MANA          | ATR_MANA           | ATR_MANA           |
|  3 | ATR_MANA_MAX      | ATR_MANA_MAX       | ATR_MANA_MAX       |
|  4 | ATR_MADNESS       | ATR_WILL           | ATR_STRENGTH       |
|  5 | ATR_MADNESS_MAX	 | ATR_WILL_MAX       | ATR_DEXTERITY      |
|  6 | ATR_STRENGTH      | ATR_STRENGTH       |--------------------+
|  7 | ATR_CONSTITUTION	 | ATR_DEXTERITY      |
|  7 | ATR_DEXTERITY	 |--------------------+
|  8 | ATR_THIEVERY      |
|  9 | ATR_SWORDSMANSHIP |
| 10 | ATR_ARCANE        |
| 11 | ATR_WILL          |
+----+-------------------+
```

They were reduced from 10 (6 primary, 4 secondary), to 5 in 0.94k to 4 in the release version.

Somewhere between 0.64b and 0.94k all the old "first order" attributes except of Strength were removed; only the "second order" attributes remained. And somewhere between 0.94k and 1.00b `ATR_WILL` was cut and with it the initial and already highly promoted idea of psionics as an independent magic system and of Madness and Sanity as factors in the gameplay; they had been crucial before, both regarding gameplay mechanics as well as regarding the Story (think of the *Madness Waves* ("Psi Emissions")). 


### Function of Attributes

Sadly we have no description at all about the function of the six primary attributes other than that they should scale the secondary ones. The reason that they were removed from the game we may find exactly here: In lack of a function. When they didn't really serve a purpose and only seemed to add an unnecessary layer of complexity while the status attributes worked just as well on their own, they may have seen no reason anymore to keep them.  
Another reason may have been the additional workload: When characters should comment on the players level in the primary attributes, it requires lots of additional voice recording and scripting.  

Hence we cannot say anything about the possible function of attributes such as the arts, namely thievery, weaponry, arcane and will (not the associated "willpower").  

But concerning the secondary attributes, we have a short description of their "application" by Alex according to which... 
Strength is responsible for damage dealt in melee combat, for handling 2H weapons and for carrying, moving or using heavy objects. Dexterity is responsible for damage dealt in ranged combat and thief skills. Mana is the energy for magic (or "alchemical") spells and is also responsible for the resistance against magic. Will(power) is the energy for Psi-Spells and is responsible for the resistance against psi powers. Health, self-explanatory, represents the characters "life" in form of hitpoints.  


#### Mana, Will & Madness

We know that *Psi* and *Alchemy* were supposed to be two completely independent and "mutually exclusive" forms of magic. Mike refered to *Alchemy* as the magic form of the two circles of fire and water. This explains why they were also called "Feueralchemisten" and "Wasseralchemisten" in [Sleeper's Ban](https://gothicarchive.org/documents/SleepersBan.html) by Alex Wittmann (but more on that in the lore related Alchemical magic doc). This mutual exclusiveness was planned right from the start, as can be seen on a note by Mike on p.1 of the spells document collection. Since then this idea was repeated over and over in various interviews and on all kinds of promotional texts.  

On the same page we find another relevant idea of a potential magical overload:  

```
Magic = OVERLOAD
PSI = automatic deactivation
```

What he may have imagined by this overload remains speculation.  
On p.6, the correlation between Will and Madness appears for the first time:  

```
Black Soul Bar -> 100%
-> can not cast spells anymore; has to take drugs
The better the Will the less Madness increase per spell
```

There is also the following mentioning (in the `pChanges.txt` of v0.56c):

```
+ Regeneration LP,MANA,SANITY
```

What was named Willpower before (with `ATR_MADNESS` as its constant) was here described as *Sanity*, as the absence of madness, to put it into positive terms. The idea was always that Willpower protects from Madness. The changelog was written in the context of an engine update (v0.77) that also introduced the first version of the Symbol-HUD.  

Accordingly there where two contrasting approaches: Casting psi spells would increase Madness (= decrease Sanity); but while the original idea was to have this displayed by filling the "Black Soul Bar" representing that madness, the later idea and actual implementation was to display the slow loss of Sanity by a reduction of the stone symbols representing the characters sanity (or, more precisely: representing the "Willpower" as the protection against Madness).  

While Mana was supposed to regenerate automatically it was made clear in interviews that the "Willpower" does not regenerate and has to be recharged by prayer (to the sleeper idols) or by meditation.  
The early note on the "black soul bar" by Mike on the other hand speaks of a need to take drugs in order to reduce the Madness. It is not clear how (and if) those two ideas relate to each other.  


### Visualisation of Attributes

Inititally, not only skills, but also attributes should have been visualised.  

>  The character development is based on visualization. Every enhancement of your characters skills **and attributes** will be shown in graphical effects like changing character animations, there are no more character stats. (Mike Hoge, 11.06.1998, interview with IGN)

> […] It will not be sufficient to collect a mighty two-handed-sword. If you […] aren't even strong enough to wield the weapon, your blows will not only be slower and not so powerful, but you will see how your Character has got problems even raising the mighty weapon! So you've got attributes like strength and dexterity as well as many skills and spells, and every single one of them will have different animations or additional effects when you learn or improve them. (Mike Hoge, 15.06.1998, desslock.gamespot.com)


#### Visualisation vs. Representation

While the visualisation of attributes such as strength and dexterity is explained above (in theory; it was never implemented, but animations existed), there arises a need to display stats such as *Health* (HP), *Mana* (MP) and *Willpower* (WP) on the screen, due to their fluctuation during gameplay. By having both a maximum and an actual value. HP, MP and WP can be reduced, regenerated, recharged and discharged. The HUD is supposed to display and inform about these changes, to *represent* those changes, but cannot *visualise* them. 

##### Simplifying the HUD

In 1997, when they began to work on the interface, including the HUD, the minimalism they strived for was radical for an rpg; back then just a few shooters and adventures came with a similarly minimal interface. And while they could not go without a HUD completely and had to represent specific stats, they at least tried to keep it simple.  

![First Version of the Symbol HUD](/_img/mechanics/HUD/symbolHUDv1.jpg)

<p class="subtext">Above is the first version of the symbol HUD. Please note that Mana and Psi points are displayed here for testing purposes; they were not supposed to be displayed simultaneously in the game.</p>

At first the six attributes (later five) were represented as symbols (hearts, stars, fists etc.). At some stage experience points were included; where a specific number of Exps would be represented by little Exp coin symbols, that were to be invested to learn from teachers. Here this was made clear by Alex, translated by us:  

> Attributes are controlled by integers between 1 and 20. The attribute values are displayed via an equivalent number of symbols. This has the purpose, that all processes in the entire game can be summed up with simple symbol quantities. This does not only apply to attributes, but also for weapon damage, armor protection, spell costs, spell damage, experience and so on. (`Phoenix_B1_AttributesTalentsActions.doc`)

Later (in ~v0.8) a brutalist bar design was implemented to represent the attributes instead. The red health bar for instance could now be seen as representing the amount of (healthy) blood in the player character that he looses in battle when bleeding. Strength and Dexterity were no longer represented; the psionic system and the Will(power) attribute was no longer in use (we don't know if deliberately discarded or cut due to time restrictions).  

This first bar design should not be confused with the one used in the release version. It followed the same idea as the initial symbol design, where NPCs with less HP/MP/WP would have less corresponding symbols. Here they would have a smaller bar.

![Alpha Version of the Bar HUD](/_img/mechanics/HUD/bar-hud.png)

<p class="subtext">Note the darker, inside part in the Mana bar, the actual maximum degree of Mana this specific character can recharge; the outside bar represents the maximum degree to which the character could level his Mana in course of the game. In the release version the bar would be stretched to always cover the background texture.</p>

This way the bars - potentially - could have been providing more information, because the player could recognise how much HP an enemy had. We say "potentially" because actually both in the symbol hud as in the bar hud the HP of NPCs in focus was displayed differently than the stats of the player himself. By a narrow, stretched out bar with no such information provided. They used a smaller version of the HP bar above with the Bar-HUD, while they used the one below to display enemy health with the Symbol-HUD:

![HP of NPCs in Focus](/_img/mechanics/HUD/hp-of-npc-in-focus.jpg)

The HUD was additionally simplified by hiding all the bars that were not currently in use; in the symbol HUD, strength and dexterity would only appear when in the melee or ranged fighting mode. Mana and Psi Power would only appear when in the respective magic casting mode. 
Just the Health was decided to be displayed at all times for reasons unknown. Thus, other than the Health Symbols/Bar, the HUD was hidden completely and only shown when needed.  

The inventory was also hidden by default and could be toggled on or off; which, while being a standard today, was not the default in classical rpgs. By displaying items in the inventory as 3D models just as they are actually found in the game - instead of using abstract pictograms as most games do - another step was done to reduce unnecessary abstractions.  

While both HUD designs managed to *represent* those stats of the player and to simplify this representation to the bare minimum, they remained abstract and reveal a lack of visualisation.  


##### Overcoming the HUD

As said before, the need for the HUD arises primarily in order to display and inform about the changes of Attributes like Life (HP), Mana (MP) and Willpower (WP). In order to overcome this need one would have to find ways to visualise these changes. At least seeds of this idea were already present in the Alpha.  

![Wounded Overlay in v0.64b](/_img/mechanics/visualisation/overlay_wounded.gif)

In v0.64b, if you are injured, the player character stands and walks with an extra animation overlay, slowly hobbling, pressing his hands on his wounds as if to stop the bleeding; combined with visual bleeding effects and sound design to intensify the pressure as the HP of the player decrease, this solution would have made the health bar redundant. 
It was not implemented in the end, be it by lack of time or by deliberate decision, but based on what we know and described so far, it would have been the next logical step, following the vision of radical visualisation they initially proposed and promoted.  



## Phoenix Attributes

In the past when we only had access to the list of alpha attributes (from the `worldfile.txt`) without any context and without any of the related documents or builds that we analysed above, we could only guess their meaning.  

We didn't know about Mikes early idea of a "black soul" bar, we didn't know for sure about a relation between Madness and Will, about Mikes handwritten attribute lists and of the correlation of different attributes. All these insights were only made possible by our [rescue of the design concepts](https://phoenixthegame.com/specials/20thAnniversary/) that we digitised and published in the Archive. And yet we had come to very similar conclusions on our own.  

At first and influenced by the release system we imagined that there was some difference between attributes such as Strength, Dexterity, Hitpoints, Mana, Willpower (as the Mana equivalent for Psionics; that much we knew from the interviews), to things like Arcane, Swordsmanship and Thievery. Following the original german terms (*Waffenkunst*, *Diebeskunst*) I conceived them as "Künste" (Arts) mostly relevant for the specific skills of the four classes in opposition to the main attributes relevant for all. With the little problem that there was no fourth "art" that we would have been able to assign to the psionic. Will, while being of special importance to the psionic, we imagined to be of general importance to all and we didn't know about the correlation between Will and "Willpower".

The arts were defined by me as pre-requisites for class-specific skills ("talents") to learn and I came up with the idea of the Arts as a specific form of experience that would reward the player for using the skills of his chosen class, all in order to fortify the story-driven gameplay and at the same time to replace the general experience points, which, as various early statements suggest (see [[EXPERIENCE]]) we deemed to not have been part of the initial vision of the game. It was a neat little system to overcome any form of grinding and I am still happy with the idea.  

Another idea of mine that is not grounded in any research was to combine Strength and Hitpoints in one; the details of which we will explain below. But in short: I liked the simplicity of it, I was inclined to it for how it deviates from the usual system in rpgs and due to the interesting balancing.  

But since all the attributes were just mixed up in the scripts the main aspect that we only became aware of through the acquisition and research of the design documents was the difference of first and second order attributes and their correlation that we now had to consider and to explain.  


**Reconstructing the first order Attributes**

In striving to finish the game it might have been reasonable to remove the "first order" attributes, but based on how they were the initial idea, since they were part of the concept for so long and due to their strong correlation with the classes - which to fully realise is one of our primary goals - and how their remnants inspired our imagination for years, we will have to reconstruct the "first order" attributes. We will find good reasons for them to persist and we will equip them with meaning in context of the setting as well as for gameplay.

We have to analyse the difference between those attributes which are relevant for all classes and those which are optional or even mutually exclusive.  


### Strength, Constitution, Hitpoints and Damage 

Constitution is relevant to everyone and with no primary focus on any class. 
Strength is primarily relevant and skilled by Warriors. Mages and Psionics may not skill it at all, but it is nonetheless a factor that matters to every character; it sets limits of how you can or can not interact with the world. Everyone will have some degree of Strength.

Strength and constitution have to be closely interlinked. Strength has to scale the DP (damage points), constitution has to scale the HP (hit points). In this sense they represent the damage that the character can inflict and the damage he can endure.   

Now, Mana and Willpower according to Alex' description define both magic/psi damage as well as the resistance against magic/psi. Why shouldn't this be the case for strength too? So in our system, while both strength and constitution exist internally and will also be referred to by NPCs, one who can deal more damage can automatically endure more damage and vice versa. It is your overall physical "Kraft" (strength) that controls both. Thus:  

* `ATR_Strength` -> `HP`+`DP` 
* `Constitution` -> `REG_*`

In our system, someone who has more strength can also endure much more hits. But at the same time the regeneration takes longer and requires more energy, while for someone with low strength but high constitution, the regeneration is faster and requires less energy. In the same way someone with less strength (and therewith less body mass) can sprint longer and higher constitution results in faster regeneration of the sprinting meter (displayed like the oxygen bar).  

[Add stuff from google docs!]  



## Dexterity 

TODO!!


### Will, Psi & Madness 

How about Will? In the way that will was planned and used in the Alpha, it was solely associated with psi magic and protection against the same. *Only* psionics had any amount of will, everyone else had none at all and they would only be protected against psionic magic via psi-protective armor pieces, amulets and so forth.  

We think that this is not convincing and more importantly, that it greatly misses all the other ways in which we can utilise will in the game world. Before we knew anything on how the attribute was supposed to function in the Alpha, Arbax imagined that the willpower of npcs and the player character would be important in dialogues, since the psionic would not just use spells but he could use dialogues to intimidate others, he could force his will on others by words and depending on their own will they would be able to resist or give in to such attempts.  

And the same for such things as control. When the psionic attempts to control an npc success should depend on his will being stronger than the will of his opponent. With this notion how would it make any sense that a digger can be intimidated or controlled as much as a baron?  

And this is also not as it was actually planned in the earliest docs by Mike. In various notes on spells he wrote how the success of a spell depends on the enemies willpower. TODO: is that so?  

The values as they were distributed in 0.94k seem not to be consistent with this idea. Instead, every npc has to have some amount of will and npcs of higher levels should automatically have higher will. But how can that be the same as the "willpower" in the sense of the psi energy, of which YBerion has to have most among the humans and the Sleeper himself must have an abundance of?  

Here we come to the meaning and importance of the will and psi-energy correlation. Only psionics should have psi-energy; that is what they themselves refer to as "willpower", but that is in reality a kind of demonic force. This willpower is what is left in 0.94k (since that only contains the "secondary" attributes) and in this sense it makes sense how non-psionics have no amount of willpower (= Psi). Every npc should have some amount of *Will*, but it should not be confused with the willpower of the psionics. The two terms continue to cause confusion, therefore we will refer to willpower as *psi-energy* from now on.  

The correlation of will and psi-energy is that while someone with a strong will may not have any psi-energy, someone with psi-energy (or psi-power-potential) will automatically have more of it when he has a strong will.  

Example: Gomez will have 10 Will (highest) but 0 Psi.  
YBerion will have 10 Will but 30 Psi.  

Will is a primary attribute of which 10 levels exist for everyone. Psi is a correlated and class specific attribute that has to be acquired in course of the story by joining the sect.

```
+--------------+
| Will | ≤ Psi |
|------+-------|
| Lv1  |     3 |
| Lv2  |     6 |
| Lv3  |     9 |
| Lv4  |    12 |
| Lv5  |    15 |
| Lv6  |    18 |
| Lv7  |    21 |
| Lv8  |    24 |
| Lv9  |    27 |
| Lv10 |    30 |
+--------------+
```

In this way, the level of Will determines the *potential* of psi-energy usage before drifting into madness.

<p class="subtext">For monsters, psi is scaled by factor 2. Thus, the Sleeper at Lv10 has 60 Psi.</p>

At the same time it is WILL that controls the resistance against Psi.  

But we also have to consider madness. Here we are confronted with the two contrasting approaches that are mostly about representing madness or sanity in the HUD. WILL is an absolute value that cannot be diminished. Psi-energy has an actual and a maximal value that can be exhausted and recharged. And there are two kinds of PSI:  
One is the psi energy handled by a psionic and represents the maximum amount of demonic force a psionic can handle. The other is the environmental psi energy in form of psi emissions, in form of localised psi-rays at so called "psi-knots" and in form of the general psi radioactivity in the atmosphere that increase in course of the story and from emission to emission. 

<p class="subtext">While the psi-energy of psi-npcs is automatically scaled by their will from 0 to 30, player characters have to find Psi-knots in the game world to increase their psi-energy.</p> 

The psi-energy of the psionics can be fend of by enough Will. The localised psi-rays can be avoided by keeping distance from psi knots or external protection. The psi emissions and general radioactivity past a certain point can only be endured by drugs or strong external protection.

The condition that most NPCs won't have any access to such drugs anymore nor any kind of psi protection - while the psi forces in the environment keep being increased - will be the primary reason for the *Nemesis*; more on that in [[#Alpha Story]]. But without a dedicated madness value independent from the psionic-exclusive willpower, nothing about that could be displayed in the game as originally intended.

Based on these ideas, it is simply not sufficient to have Will as described before and the psi points as exclusive energy of psionics like mana points as exclusive energy of mages. Madness cannot be the lack of the primary Will attribute, since that is an absolute value, nor can it be just the lack of psi energy; if 0% psi would equal 100% madness everyone but the psionics would be mad and a psionic player could never fully exhaust his available psi-energy. Thus, the psi-energy or willpower that is psionic-exclusive can not equal the sanity or madness meter that should be relevant to all npcs.  

We assume that this complex relation and interconnection, while it may vaguely have been at the back of ones head, was never properly documented, it was confusing and thus was confused in the actual implementation in the engine and the alpha builds and we attempt to dissolve this confusion.

In consequence there arises the need to add Madness *additionally* and *independently from Psi*, where another of my old concepts comes into play that I developed in the end of 2018:

Madness is negative Willpower.  

That said: The Will of an NPC protects from Psi attacks and thus from madness -> since attacking someone in the psionic way basically means to drive him mad. But at the same time, dealing with psi energy in such a way is dangerous. As Tom Putzki told us, quoting one of his favourite lyrics, *"Der Wahnsinn ist nur eine schmale Brücke"* (Madness is just a small bridge), but more correctly I would say: *Sanity is a small bridge and Madness lies beneath* and the psionic is always on the edge.  

We will not let psionic casting "automatically end" as the early note by Mike suggests, instead it will become a gameplay factor for the player to know the mental capacity of his characters and be on or close to this edge and decide how much he can lean beyond. 
When he deals with the energy beyond his treshold (when all Psi-Energy points are used up or when the psi bar is fully discharged), the madness (in form of the black soul bar or new dedicated madness symbols) begins to fill.   

While it is safe to say that this was never actually planned as such and that this is our original solution that we came up with just based on the terms Will and Madness before knowing about the concepts behind it, it may actually be the only way in which we can include both the psi energy discharge as implemented in the game and the "black soul bar" idea of increasing madness from Mikes concept; our solution combines and harmonises both.

Thus, in this context we need the following attributes:  

* `ATR_WILL` 
* `ATR_MADNESS` 
* `ATR_MADNESS_MAX` 
* `ATR_PSI`
* `ATR_PSI_MAX`


### The Arts 

After clarifying the general attributes, the "Arts" remain. But which purpose do these arts serve in the gameplay? What is their function?

TODO!!!


While before in the alpha research we correlated Arcane, Weaponry, Thievery and Will to the four classes, Will does not really fit into this scheme and the system proposed here. It wouldn't be consequent due to how important Will is for every character and independent of the class compared to Thievery and Weaponry that are clearly class focused.  

One approach would be to argument that while the psionic magic and the alchemical magic are completely independent, *Arcane* may work as an overarching attribute of magical knowledge for both magical classes. But that doesn't fit because one of the essential characteristics of psionics in classical roleplaying games is exactly their despise of the "Arcane" that stands for the traditions and rituals of the clerics (here of the cults of the realm with the mages as priests).  

Thus, either we would have to go without a psionic equivalent to the three Arts for the other classes (which would be inconsequent) or we have to come up with something more suitable to the heretic nature of the psionics, which is obviously what we do. Adding "psionics" as an art.  

In the same way as the arcane art opens the mind and prepares the body of the mage for the mana, a psionic art has to open the mind and prepare the body of the psionic to the psi energy. Opening the mind and preparing the body for the psi energy means to enable him to see/sense this energy in the first place (such as in form of the psi-knots) and to learn handling it. So what this psionic art has to be about is not the arcane, but a psychic or mystic sense.  

Just as the mage can lead the way to the magical ore (that he needs for his potions which again he needs to boost mana) due to his ability to alchemically sense physical substances that are magically charged, having a whole set of additional perceptions unknown to those without the *Arcane Gift*, in the same way there are additional perceptions to the highly skilled psionic, opening up a world beyond the physical and allowing him a glimpse into the mystical, psychical (or demonic) reality like an overlay over the world perceived by others, by which, for instance, he can see the psi-knots that he needs to boost his maximal psi-energy and other phenomena.  

The psionic brotherhood (which was highly inspired by buddhism in fact), uses the sign of the opened eye. And the open eye signifies awakening. That is exactly what the psionic art has to be about, what they all are working on: to awaken.  

The warrior strives to master combat and weaponry. The thief strives to become a master thief, to master thievery. The mage strives to dive into the arcane knowledge and to reach the highest initiations. And the psionic strives to awaken himself and thereby the sleeper and to awaken the sleeper and thereby himself; one through the other.  

Thus we need the following "arts":

```
     +---------------------------+
     | Künste      | Arts        |
+----|-------------|-------------|
| DK | Diebeskunst | Thievery    |
| WK | Waffenkunst | Weaponry    |
| AG | Arkane Gabe | Arcane Gift |
| PG | Psi Gabe    | Psi Gift    |
+--------------------------------+
```




#### Thievery

Thievery is obviously relevant for thieves and while thieves may be able to reach some degree of Weaponry (his dagger-tricks are thief-skills and thus not associated with Weaponry).


#### Weaponry 

Weaponry is primarily relevant for warriors.  
TODO: Explain how it scales dex and skills in npcs?


The Arcane Art does not really matter to anyone but the mages, but one may still acquire a bit of arcane knowledge by chance, the psionics may steal knowledge from the mages and so on. The important thing is that they won't get any Mana -> this is mage exclusive.  





### Completing the clear texts

Based on the incomplete and work in progress texts from v0.56c, we have to come up with a complete structure for the ten levels of attributes analysed before (and those added by us). The list is <span class="added">work in progress</span>.  


<pre>
|    | Kraft          | Konstitution     | Wille          | Waffenkunst   | Diebeskunst    | Arkane Gabe | <span class="added">Psionik</span>      |
|----|----------------|------------------|----------------|---------------|----------------|-------------|--------------|
|  1 | gelähmt        | <span class="changed">halbtot</span>          | <span class="changed">besessen</span>       | keine         | keine          | <span class="added">keine</span>       | narkotisch   |
|  2 | schwindsüchtig | komatisch        | willenlos      | wehrlos       | unbeholfen     | <span class="added">Kreis 1</span>     | schlafend    |
|  3 | schwächlich    | kränklich        | willensschwach | unsicher      | tollpatschig   | <span class="added">Kreis 2</span>     | träumend     |
|  4 | schwach        | <span class="changed">anfällig</span>         | unsicher       | wehrhaft      | ungeschickt    | <span class="added">Kreis 3</span>     | fantasierend |
|  5 | kräftig        | robust           | <span class="added">zaghaft</span>        | treffsicher   | geschickt      | <span class="added">Kreis 4</span>     | eingekehrt   |
|  6 | stark          | widerstandsfähig | <span class="added">gefestigt</span>      | <span class="changed">sehr behände</span>  | fingerfertig   | <span class="added">Kreis 5</span>     | durchbrochen |
|  7 | bärenstark     | athletisch       | entschlossen   | Meister       | meisterhaft    | <span class="added">Kreis 6</span>     | geblendet    |
|  8 | unbezwingbar   | zäh wie Leder    | unbeugsam      | ...           | Fingerkünstler | <span class="added">Secret</span>      | versunken    |
|  9 | <span class="added">Secret</span>         | <span class="added">Secret</span>           | <span class="added">eisern</span>         | ...           | ...            | <span class="added">Secret</span>      | erleuchtet   |
| 10 | <span class="added">Secret</span>         | <span class="added">Secret</span>           | <span class="added">frei</span>           | <span class="added">Schwertsänger</span> | ...            | <span class="added">Secret</span>      | erwacht      |
</pre>


### Phoenix HUDs

The HUD will be optional and it will be possible to play without ([[#Beyond the HUD]]).
We will provide both the symbol HUD and the v0.8 bar HUD as options in the menu. 
We use improved versions of both of them and you can toggle them on or off.
We hide the HP Bar/Symbols during exploration mode when not wounded.  


#### Enhanced Symbol HUD

Sasha (aka Jr) was inspired by the Symbol HUD of the alpha versions and started to develop an enhanced version of it. There was no symbol to represent oxygen when diving, so he added a little bubble symbol. Since he imagined that one symbol such as HP does not necessarily correlate to one health point internally, but may be the sum of a specific number of healthpoints, he included an optical transition. As we know now one symbol should exactly correlate to one health point, such that this idea has become redundant.  
In cooperation with me he later improved the HUD even further and designed it to our liking; he included the possibility to switch between the Symbol- and Bar-HUD from the menu, provided options to customise the HUD to ones liking and included Phoenix presets (such as hiding HP when not injured).  

![Corristos HUD example HP & MP Level 2+3](/_img/mechanics/HUD/HUDCor.png)

Psi Symbols:  

![Psi HUD example Level 1+2](/_img/mechanics/HUD/HUDPsi2.png)

Based on an idea by Alex mentioned in the documents, we add new strength symbols for different species, such as these for Gobbos and Orcs:

![Gobbo HUD example Green Fists](/_img/mechanics/HUD/HUDGobbo.png)

![Orc HUD example Fists](/_img/mechanics/HUD/HUDOrcSlave.png)

New dedicated Madness Symbols:

![New Madness Symbols](/_img/mechanics/HUD/HUDMad2.png)


#### Enhanced Bar HUD

The bar HUD will follow the brutalist style and function from ~v0.8-0.9.  
Just as the Symbol HUD the bars will be smaller for characters with smaller values and larger for characters with larger values, not being stretched to a fixed width. Instead of adjusting the bars to the background texture, we will adjust the background texture to the bars. This will not only provide additional information to the player, the HUD will also cover less of the screen.  


### Attribute Visualisation or Beyond the HUD

Allow me the pathetic metaphor: Just as "that government is best which governs the least" (Thoreau), because it creates conditions of self-regulating autonomy under which its intervention isn't needed anymore as the people are able to govern themselves; that HUD (heads-up display) is best which has to be displayed the least, because the developers created conditions of self-explanatory gameplay mechanics by which its representation isn't needed anymore as the players are able to play it themselves. A metaphor for Gothics minimalist interface design.  

And just as we aren't demanding for the government to just be taken down, but for it to remain fully functional if necessary while realising it as its primary function to make itself unnecessary (at which all governments fail, thereby undermining their own legitimacy); and to the same degree as the government is needed, to this very degree it exposes the lack of autonomy established in society which it needs to govern less (and for us to be more free) - In the same way we aren't demanding to eliminate the HUD, but we want that it is not *needed*, because to the same degree as the HUD is needed, to this very degree it exposes a lack of visualisation established in the gameplay which we need for less abstraction (and for us to play more directly).  

This said, we do not strive to get rid of the HUD altogether, but we want it to be optional and for the game to be fully functional (= playeable) without it. 

The HP reduction will be visualised by enhancing the idea experimented with in v0.64b as described in [[#Overcoming the HUD]]. Before seeking refuge in pfx effects we have to consider equivalent solutions of animations for the discharge and exhaustion of Mana and Psi. Their visualisation has to be strongly correlated with how these attributes function.  

Just as there is an overlay when the character is injured - has less than X HP -, there will be an overlay when the character has less than X Psi- or Mana points. When the psionic reaches the end of his Psi treshold, the demonic force begins to pressure him and he gets headaches; at this point he will walk around with his hand on his head, turning and shaking his head while standing, not being able to run, signifying to the player that his character is on the edge and madness is nigh.  
This will be accompanied by a droning sound effect and a mild visual effect.  

<p class="subtext">Related fun fact: Mike wrote in his notes that psionics should only be able to cast psi spells as long as they don't wear a helmet.</p>

While the animation overlay of the psionic visualises how his magic is mainly associated with his mental power by laying the focus on his head, the magic of the Arcane Mages is different, alchemical and associated with the Mana in his bloodstream (more on that in [[#Alchemical Magic]]). Hence when he is close to the edge of Madness his overlay has to show how the lack of Mana (that serves as a physical protection from the demonic forces just as the Psi serves as a psychical protection) is affecting his whole body similar to an addict on withdrawal. He will be shown bent over, scratching his arm or looking at his hand. 


#### Possession

When X points of madness are reached, a character is possessed. When he reaches this state his eyes turn red (texture change) as described in Alex Story (and as shown in form of the fanatics in the release version of the game). Lower level characters will flee when perceiving someone in the possessed state, unless they are possessed themselves. Characters on the same or a higher level (when neutral or angry) will draw their weapon/magic and shout at him to go away.  
Friends will immediately speak to him and try to help him with drugs if they have any. But more than that: When the player character is possessed, the player will not be completely in control anymore. His character will do things against the will of the player for the player to experience being unwillingly controlled.  
He is then in a fight between the influences of the demonic force and of what he wants to do himself. The force drives him towards violence and blood; he has to struggle against himself and regain sanity before it is too late.  


### Summary

In order to structure these mixed attributes, we asked the question what attributes usually stand for in a roleplaying game.  

> An **attribute** is a piece of data (a statistic) that describes to what extent a fictional character in a role-playing game possesses a specific natural, in-born characteristic common to all characters in the game.  

Based on this definition the arts are impossible to consider as attributes, since they are no characteristics common to all characters nor are they natural or inborn. The ones that would fit that description are the following ones which we could structure in a scheme like this:  

```
`ATR_CONSTITUTION` = Körperliche Verfassung
`ATR_STRENGTH`     = Körperliche Kraft 
`ATR_DEXTERITY`    = Körperkontrolle

`ATR_MADNESS`      = Geistige Gesundheit
`ATR_WILL`         = Geistige Kraft 
`ATR_PSI`          = Geistige Kontrolle
```

Psi would fit into this scheme as mental control; but as almost no one has control over his mind it is not to be seen as a general attribute yet; everyone has some degree of dexterity, but regarding the mind, most characters in the game are not in any kind of control of their mind independent from the sheer force of wanting or mentally resisting, they can't stop the stream of thought.  

Thus, the rest is either a mere representation of these for the player in form of the HUD or it has to belong to the specific experience in the Arts or "Gifts":  

```
Class specific:       Class crossing:

`EXP_WEAPONRY`        `EXP_ALCHEMY`
`EXP_THIEVERY`        `EXP_METALLURGY`
`EXP_ARCANERY`        `EXP_ARCHERY`
`EXP_PSIONICS`        `EXP_HUNTSMANSHIP` 
```

Weaponry signifies the skill as a Warrior.  
Thievery signifies the skill as a Thief.  
Arcane   signifies the skill as a Mage.  
Psionics signifies the skill as a Psionic.  



Based on all the reasoning above, this is our solution.  
Making for a coherent system, that is both simple and complex.  

There are 2 pairs of general Attributes   
refered to by clear texts:  

* Physical Condition: Constitution / Strength  
* Mental Condition: Will / Madness  

Increasing strength automatically increases Will by a factor of 0.5 and vice versa.
There are four class specific attributes:  

* Force / Dexterity  
* Mana / Psi  

There are four Status Attributes supposed to be displayed in the interface or by other audio-visual means.  

* Life (refered to as 
* Mana (refered to as "magische Kraft")
* Psi

Closely related are the Arts:  


All of these values are refered to inside the game.  


**General/primary values + correlated Status Attributes:**  
`ATR_Strength` -> `ATR_HITPOINTS`, `DMG_*`, `REG_SPECIAL`  
`ATR_Constitution` -> `REG_LIFE`, `REG_STRENGTH`  
`ATR_Will` -> `ATR_Madness`, `REG_SANITY`, `REG_FOCUS`  

**Arts + correlated Status Attributes:**  
`ART_Weaponry` -> `ATR_FORCE` + `FGT_Delay` + `FGT_SpecialAt`  
`ART_Thievery` -> `ATR_DEXTERITY` + `STL_Risk` + `STL_Focus`  
`ART_Arcane` -> `ATR_MANA` + `RESIST_MAGIC`, `REG_MANA`  
`ART_Psionics` -> `ATR_PSI` + `RESIST_PSI`, `REG_PSI`  

**Regeneration Categories:**  
General: `REG_Life`, `REG_Strength`, `REG_Sanity`  
Class specific: `REG_Special`, `REG_Focus`, `REG_Mana`, `REG_Psi`  

**Experience Categories**:  
primary: `EXP_Suffering`, `EXP_Resistance`, `EXP_Exhaustion`, `EXP_Madness`  
secondary: `EXP_Combat`, `EXP_Stealth`, `EXP_Arcane`, `EXP_Psi`  

tertiary: `EXP_Alchemy`, `EXP_Huntsmanship`, `EXP_Marksmanship`, `EXP_Metallurgy`.  `EXP_Philology`

**Damage Categories:**  
DMG_*

**Protection Categories:**  
PROT_*  

BREATH_..  
STAMINA_...  

**Resistances**  
RES_WEAPONS  
RES_POISON  
RES_MADNESS  
RES_MAGIC  
RES_FIRE  


### Attribute Scaling

Körperliche Stärke+ skaliert automatisch die Willenskraft um einen Faktor 0.5 oder so.
Also wenn man + 10 Stärke kriegt, hat man auch + 5 Willenskraft.  

Umgekehrt skaliert Willenskraft+ auch die Stärke um einen Faktor.  
So simulieren wir, wie Krieger im Laufe ihres körperlichen Trainings auch Willenskraft dazu gewinnen und wie sich umgekehrt hohe Willenskraft auf körperliche Kraft auswirken kann, während wir zugleich ein Balancing-Problem lösen.  
