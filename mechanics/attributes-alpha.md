# Alpha Attributes 


**Author:** Flosha  
**Status:** <span class="changed">Work in progress</span>  

At first we'll analyse the attributes as imagined in the concept phase by analysing all the available design documents. Then we look at the attributes as they were implemented in the actual builds of the game and how they changed in course of development. 

In the second part, building on this research, we present our own solution for Phoenix. 

**Content:**  
1. [Primary & Secondary Attributes](#primary--secondary-attributes)
2. [Attribute levels in text form](#attribute-levels-in-text-form)
3. [Attribute Progression](#attribute-progression)
4. [Default Attribute Values for NPCs](#default-attribute-values-for-npcs)
5. [Attributes & Classes](#attributes--classes)
6. [Cut Attributes](#cut-attributes)
7. [Function of Attributes](#function-of-attributes)
    1. [Mana, Will & Madness](#mana-will--madness)
8. [Visualisation of Attributes](#visualisation-of-attributes)
    1. [Visualisation vs. Representation](#visualisation-vs-representation)
        1. [Simplifying the HUD](#simplifying-the-hud)
        2. [Overcoming the HUD](#overcoming-the-hud)


## Primary & Secondary Attributes

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

`We` as *Weisheit* (Wisdom) and `Wa` as *Wahnsinn* (Madness) remain speculative but likely. `SK` on the other hand was hard to make sense of. We thought of *Schnelligkeit* (speed), *Sprachkunst* (philology) and *Streitkunst* (disputation). They all seemed unlikely for different reasons.  
Then I had the idea of it refering to *Schwarze Kunst* ("Black Art"), in the sense of the *Dark Arts* (a term as it is used in the description of the robe of Xardas (*Robe der Dunklen Künste*  = Robe of the Dark Arts)), that refers to such things as necromancy and invocation. But then Wunddorn came up with the idea of *Schießkunst* (marksmanship). Although I am fond of my *Dark Arts* idea, Marksmanship seems most likely to be the meaning of `SK`. 

Note that there is no mentioning of healthpoints or mana in the list.  

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

The first table points at a correlation between Strength `STR` and Constitution `CON`, the second at a correlation between Strength and Hitpoints `TP` (*Trefferpunkte*, which in this context should be the damage points you deal), while Constitution is here related to Healthpoints `LP` (*Lebenspunkte*, refering to the hitpoints of your character; the damage you can endure).  

Arcane Gift `AGa` (*Arkane Gabe*) is correlated to Mana. Will `WIL` (*Wille*, the psi-energy) is at first correlated to an identical attribute name, then to `WS`, which may either stand for *Willensstärke* (Willpower) or *Wahnsinn* (Madness); both terms were used inside the game at different points.  
This search for a name and differentiation between Psi/Will, Willpower, Madness and Sanity continues during development and will also be seen inside the builds we will analyse further below.  

The abbreviations `KaGe` and `DiGe` have to stand for *Kampfgeschick* ("combat skill") and *Diebesgeschick* ("thief skill") respectively. Otherwise they were named `WK` (*Waffenkunst* = Weaponry, which in the builds was called `Swordsmanship`) and `DK` (*Diebeskunst* = Thievery). While on the second table they were not put into correlation with another attribute, in the first one they were. Thievery was most likely associated with Dexterity `GE` (= *Geschicklichkeit*) and Weaponry with `AT`, which, as far as we know, simply stands for Attack.  

Mike also considered endurance/stamina (German: Ausdauer) as a potential factor on the same page, but discarded it immediately:

> ~~AUSDAUER?~~
> NO

From the first list that we think of as the original pool of attribute ideas a few were already discarded, such as `We` (Wisdom), `SK` (assumed to be Marksmanship) and `CH` (assumed to be Charisma), while `Wa` (Madness) was put into "second order". The rest remained.  

This structure remained almost unchanged for a long time in development. The same six attributes as seen on the two tables above appear in a later (typed) document by Mike, - `Phoenix_B4_Learning.doc`, p. 4 - changed last at 06.07.99, now with the full meaning given:

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

While in a document written by Alex Brüggemann - `Phoenix_B1_AttributesTalentsActions.doc`, changed last at 21.07.99 - only five attributes were listed. Constitution, Thievery, Weaponry and Arcane Gift are not mentioned at all.   

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

To add additional confusion, both the five and the six attributes can be found in v0.56c-0.64b simultaneously. While the `constants.d` in both versions lists the six attributes mentioned by Mike, the `text.d` contains just the list of five.  

Somewhere between v0.64b (07.1999) and v0.94k (10.2000), the `constants.d` was adjusted to the five attributes as they were structured in the `text.d` since at least v0.56c. So while they did co-exist for quite some time and were in some way associated with each other, at some later point it was decided - for unknown reasons - to remove the original attributes. 

Gladly in the before-mentioned doc by Mike - `Phoenix_B4_Learning.doc`, p. 5 - there is a little note with an explanation that is able to dissolve the confusion:  

> **Progression of maximal status attributes**  
> When the player increases Constitution, his LP<sub>max</sub> are increased too, the same with Arcane Gift -> MP<sub>max</sub> and Will -> WP<sub>max</sub>. When this occurs, a slow increase in length of the bar maximum can be seen inside the status screen, which displays the increasing status attribute as a (more or less filled) bar.  

Based on these findings we can conclude that the original idea by Mike - persisting for at least two years in development - was to have the six primary attributes listed above which names were supposed to be referred to inside of the game and that were responsible to scale the secondary "status attributes", which, for reasons of immersion, were not supposed to be referred to inside of the game and instead should have appeared *only* in form of symbols or bars in the user interface.  


## Attribute levels in text form

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
}
```

You may notice that there are *seven* attributes in the ``text.d``, the six primary attributes and `ATR_HP`. These "HP" are not to be confused with the `ATR_HITPOINTS` of NPCs. They're described as *Strukturpunkte* (structure points) in the associated comment and as such they are the hitpoints of *items*, which is also confirmed by the wording above (such as "unbrauchbar" (= unuseable), referring to the condition of a broken item).  

It is safe to assume that NPCs should have referred to the first order attributes inside of the game using such descriptive words as a feedback for the player; for his character progression, for the condition of items in trading and so forth. I call this concept *Immersion durch Verbalisierung* (= immersion by verbalisation). Thus they would talk about the strength and constitution, the arcane gift, the weapon and thief skills and the will / madness of the player and other characters, while not referring to the more abstract and internal *points* in form of the correlated, secondary or deduced attributes: Hitpoints, Willpoints and Manapoints.  

Some of the first order attributes are still mentioned in the release version of the game, such as *Arcane* in form of the ingame book *Elementare Arcanei* ("Elementary Arcanery") and in *Machtvolle Kunst* ("The Mighty Art"), which is introduced as: *Ein Werk für den Eingeweihten der Arkanen Kunst* (= A work for the Initiated of the Arcane Art).  

If the first order attributes were ever supposed to appear in the character profile they would have appeared in the described text form per level; while the second order attributes wouldn't have been mentioned ingame at all and would only be displayed in the interface by associated symbols or bars.  

<p class="subtext">Not all the bars on the HUD were direct representations of the status attributes. For instance in later versions there is a bar representing the oxygen when being underwater. This is not linked to an attribute but controlled by a guild value in the species script, as Auronen pointed out. There is a <code>SWIM_TIME</code> and a <code>DIVE_TIME</code> defining the swim / dive endurance before receiving damage.<br>  
While Mike discarded the idea of endurance as an attribute on its own, there was obviously a need to restrict the dive time. In the same way we can imagine that you were not supposed to be able to sprint infinitally. But instead of restricting the feature (by something like Endurance or a value like <code>SPRINT_TIME</code>) they removed the sprinting on key press and linked it to speed potions.</p>


## Attribute Progression

Mike referred to the primary attributes just as "the six attributes" or as "character values". In `Phoenix_B4_Learning.doc` he explains that these six attributes can be learned / increased from teachers just as talents and spells. Upon increase of one of the six primary attributes, the associated secondary attributes (that he referred to as "status attributes") are increased alongside.  

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

But in `Phoenix_C2_Monsters` and almost in the same way in the remnants of a later version of the Phoenix Concept, which were also written by Alex, they are structured like this (`RS` stands for Resistance):  

```
+------+------+------------+------+-----------+------------+
| LE   | RS   | STR        | DEX  | MAN       | WIL        |
|------+------+------------+------+-----------+------------|
| 5-20 | 0-10 | 1-10 (15?) | 1-10 | 1-10 (15) | 1-10 (15?) |
+------+------+------------+------+-----------+------------+
```

Accordingly in v0.56c-0.64b the NPCs had at most 20 HP, 10 Str (with one exception of 30), 10 Dex, but the maximum Mana and Madness value have been increased to 20. Even in v0.94k the character value progression was still basically following this old structure but now with a maximum Health, Will and Mana of human NPCs of 30, while the maximum Strength and Dexterity was 15.  

In course of this research we discovered and summarised some defaults.  


## Default Attribute Values for NPCs

0.94k is the most valuable source (among those available to us) to analyse the (status) values of the different guilds and ranks of NPCs. Although values vary for individual NPCs with their unique traits, we could identify a consistent set of light, medium and heavy default values:  

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

Default attributes for Monsters were a bit different. Monsters had up to 50 HP, Strength and Dex. In 0.94k, most monsters didn't have any Will or Mana Attribute associated with them (anymore), with the exception of the Wolf with 2 Mana and 2 Will. In the Gothic Gameplay Trailer from 2000 you see this system in action where the Troll has 30 HP, as Dmitriy pointed out; the Demon for instance seems to have 30 Str.  


## Attributes & Classes

We should also indicate that the initial attributes seem to have been envisioned with the four classes in mind. We can assume that they would have been heavily correlated with the class specific character progression; just in which way remains speculative.  

* **General:** Strength / Constitution
	* Strength -> Damage 1H / 2H / Axe
	* Constitution -> Hitpoints
* **Warrior:** Weaponry -> Strength(?), Attack(?)
* **Thief:** Thievery -> Dexterity -> Damage Bow / X-Bow
* **Mage:** Arcane Gift -> Mana & Mana Resistance
* **Psionic:** Will -> Madness & Madness Resistance


## Cut Attributes

```
ATR_ARCANE ATR_CONSTITUTION ATR_DEXTERITY ATR_HITPOINTS ATR_HITPOINTS_MAX ATR_MADNESS ATR_MADNESS_MAX ATR_MANA ATR_MANA_MAX ATR_PROTECTION ATR_REGENERATEHP ATR_REGENERATEMANA ATR_RESIST_FIRE ATR_RESIST_MAGIC ATR_RESIST_POISON ATR_RESIST_WEAPON ATR_STRENGTH ATR_SWORDSMANSHIP ATR_THIEVERY ATR_INDEX_MAX
```

Above is a list of all the technical `ATR` constants in the engine from the `Worldfile.txt` to be found in the Gothic-MDK. As you see, what we analysed before as first and second order attributes and what the devs clearly differentiated in their design concept was all mixed up in the constants. Not only was there no differentiation between first and second order attributes but there were also so called "zusätzlich als Attribut geführte Werte" (= "values which are additionally handled as attributes"), constants which were not *really* supposed to be attributes but were handled as such for technical reasons.  

Such is the case for `ATR_PROTECTION`, which was later replaced by a dedicated `PROT_*` constant for the different forms of protection, such is also the case for ``ATR_RESIST_*`` and finally for the later introduced `ATR_REGENERATEHP` and `ATR_REGENERATEMANA`; both of which were not planned to be listed among the actual attributes, both of which remained unused in the release and both of which would have worked just as well with a dedicated constant.  

In the `text.d` of v0.56c there is another case like that in form of "*Tarnung*" (disguise), which had no equivalent (either not anymore or not yet) among the constants, but just as protection it was not really supposed to be an attribute.  

<p class="subtext">In 0.56c-0.64b the maximum attribute index was 18.<br> 
In 0.94k it was 10. In 1.00b onwards it was 8.</p>

When we blend out these attributes that were only handled as such for technical reasons (usually just tempory), we end up with the following comparison of attribute constants throughout the available builds, as they were continueously reduced:  

```
+----+-------------------+--------------------+--------------------+
|    | 0.56c/0.64b       | 0.94k              | 1.00b - 1.12f      |
|  - | ----------------- | ------------------ | ------------------ |
|  0 | ATR_HITPOINTS	   | ATR_HITPOINTS      | ATR_HITPOINTS      |   
|  1 | ATR_HITPOINTS_MAX | ATR_HITPOINTS_MAX  | ATR_HITPOINTS_MAX  |
|  2 | ATR_MANA          | ATR_MANA           | ATR_MANA           |
|  3 | ATR_MANA_MAX      | ATR_MANA_MAX       | ATR_MANA_MAX       |
|  4 | ATR_MADNESS       | ATR_WILL           | ATR_STRENGTH       |
|  5 | ATR_MADNESS_MAX	 | ATR_WILL_MAX       | ATR_DEXTERITY      |
|  6 | ATR_STRENGTH      | ATR_STRENGTH       |--------------------+
|  7 | ATR_CONSTITUTION	 | ATR_DEXTERITY      |
|  7 | ATR_DEXTERITY	   |--------------------+
|  8 | ATR_THIEVERY      |
|  9 | ATR_SWORDSMANSHIP |
| 10 | ATR_ARCANE        |
| 11 | ATR_WILL          |
+----+-------------------+
```

They were reduced from 10 (6 primary, 4 secondary), to 5 in 0.94k and finally to 4 in the release version. Somewhere between 0.64b and 0.94k all the old "first order" attributes except of Strength were removed; only the "second order" attributes remained. And somewhere between 0.94k and 1.00b `ATR_WILL` was cut and with it the initial and already highly promoted idea of psionics as an independent magic system and of Madness and Sanity as factors in the gameplay; they had been crucial before, both regarding gameplay mechanics as well as regarding the Story (in the context of *Madness Waves* ("Psi Emissions")). 


## Function of Attributes

Sadly we have no description at all about the function of the six primary attributes other than that they should scale the secondary ones. The reason that they were removed from the game we may find exactly here: In lack of a function. When they didn't really serve a purpose and only seemed to add an unnecessary layer of complexity while the status attributes worked just as well on their own, they may have seen no reason anymore to keep them.  
Another reason may have been the additional workload: When characters should comment on the players level in the primary attributes, it requires lots of additional voice recording and scripting.  

Hence we cannot say anything about the possible function of attributes such as the arts, namely thievery, weaponry, arcane and will (which shouldn't be confused with the associated "willpower").  

But concerning the secondary attributes, we have a short description of their "application" by Alex according to which...  
Strength is responsible for damage dealt in melee combat, for handling 2H weapons and for carrying, moving or using heavy objects. Dexterity is responsible for damage dealt in ranged combat and thief skills. Mana is the energy for magic (or "alchemical") spells and is also responsible for the resistance against magic. Will(power) is the energy for Psi-Spells and is responsible for the resistance against psi powers. Health, self-explanatory, represents the characters "life" in form of hitpoints.  


### Mana, Will & Madness

We know that *Psi* and *Alchemy* were supposed to be two completely independent and "mutually exclusive" forms of magic. Mike referred to *Alchemy* as the magic form of the two circles of fire and water. This explains why they were also called "Feueralchemisten" and "Wasseralchemisten" in [Sleeper's Ban](https://gothicarchive.org/documents/SleepersBan.html) by Alex Wittmann (but more on that in the lore related Alchemical magic doc). This mutual exclusiveness was planned right from the start, as can be seen on a note by Mike on p.1 of the spells document collection. Since then this idea was repeated over and over in various interviews and on all kinds of promotional texts.  

On the same page we find a relevant idea of a potential magical overload:  

```
Magic = OVERLOAD
PSI = automatic deactivation
```

What he may have imagined by this overload remains speculation.  
On p.6, the correlation between Will and Madness appears first time:  

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

Accordingly there where two contrasting approaches:  
Casting psi spells would increase Madness (= decrease Sanity); but while the original idea was to have this displayed by filling the "Black Soul Bar" representing that madness, the later idea and actual implementation was to display the slow loss of Sanity by a reduction of the stone symbols representing the characters sanity (or, more precisely: representing the "Willpower" as the protection against Madness). Thus, will and madness were not seperated in the game. There was no seperate increase of madness in any version of the game.  

While Mana was supposed to regenerate automatically it was made clear in interviews that the "Willpower" does not regenerate and has to be recharged by prayer (to the sleeper idols) or by meditation.  
The early note on the "black soul bar" by Mike on the other hand speaks of a need to take drugs in order to reduce the Madness. It is not clear how (and if) those two ideas relate to each other.  


## Visualisation of Attributes

Inititally, not only skills, but also attributes should have been visualised.  

>  The character development is based on visualization. Every enhancement of your characters skills **and attributes** will be shown in graphical effects like changing character animations, there are no more character stats. (Mike Hoge, [11.06.1998, interview with IGN](https://gothicarchive.org/interviews/1998/11.06.1998_rpgvaultarchive.txt))

> […] It will not be sufficient to collect a mighty two-handed-sword. If you […] aren't even strong enough to wield the weapon, your blows will not only be slower and not so powerful, but you will see how your Character has got problems even raising the mighty weapon! So you've got attributes like strength and dexterity as well as many skills and spells, and every single one of them will have different animations or additional effects when you learn or improve them. (Mike Hoge, [15.06.1998, desslock.gamespot.com](https://gothicarchive.org/interviews/1998/15.06.1998_desslock.gamespot.txt))


### Visualisation vs. Representation

While the visualisation of attributes such as strength and dexterity is explained above (in theory; it was never implemented, but animations existed), there arises a need to display stats such as *Health* (HP), *Mana* (MP) and *Willpower* (WP) on the screen, due to their fluctuation during gameplay. By having both a maximum and an actual value. HP, MP and WP can be reduced, regenerated, recharged and discharged. The HUD is supposed to display and inform about these changes, to *represent* those changes, but cannot *visualise* them. 


#### Simplifying the HUD

In 1997, when they began to work on the interface, including the HUD, the minimalism they strived for was radical for an RPG; back then just a few shooters and adventures came with a similarly minimal interface. And while they could not go without a HUD completely and had to represent specific stats, they at least tried to keep it simple.  

![First Version of the Symbol HUD](/_img/mechanics/HUD/symbolHUDv1.jpg)

<p class="subtext">Above is the first version of the symbol HUD. Please note that Mana and Psi points are displayed here for testing purposes; they were NOT supposed to be displayed simultaneously in the game, you can only have either Mana or Psi.</p>

At first the six attributes (later five) were represented as symbols (hearts, stars, fists etc.). Experience points were included too. A specific number of Exps would be represented by little Exp coin symbols, that were to be invested to learn from teachers.  
Here this was made clear by Alex, translated by us:  

> Attributes are controlled by integers between 1 and 20. The attribute values are displayed via an equivalent number of symbols. This has the purpose, that all processes in the entire game can be summed up with simple symbol quantities. This does not only apply to attributes, but also for weapon damage, armor protection, spell costs, spell damage, experience and so on.   
`Phoenix_B1_AttributesTalentsActions.doc`

Later (in ~v0.8) a brutalist bar design was implemented to represent the attributes instead. The red health bar for instance could now be seen as representing the amount of (healthy) blood in the player character that he looses in battle when bleeding.   
Strength and Dexterity were no longer represented; the psionic system and the Will(power) attribute was no longer in use (we don't know if deliberately discarded or cut due to time restrictions).  

This first bar design should not be confused with the one used in the release version. It followed the same idea as the initial symbol design, where NPCs with less HP / MP / WP would have less corresponding symbols. Here they would have a smaller bar.

![Alpha Version of the Bar HUD](/_img/mechanics/HUD/bar-hud.png)

<p class="subtext">Note the darker, inside part in the Mana bar as the actual maximum degree of Mana this specific character can recharge; the outside bar represents the maximum degree to which the character could level his Mana in course of the game. In the release version the bar would be stretched instead, in order to always cover the background texture.</p>

This way the bars - potentially - could have been providing more information, because the player could recognise how much HP an enemy had. We say "potentially" because actually both in the symbol hud as in the bar hud the HP of NPCs in focus was displayed differently than the stats of the player himself. Simply by a narrow, stretched out bar. They used a smaller version of the HP bar above with the Bar-HUD, while they used the one below to display enemy health with the Symbol-HUD:

![HP of NPCs in Focus](/_img/mechanics/HUD/hp-of-npc-in-focus.jpg)

The HUD was additionally simplified by hiding all the bars that were not currently in use; in the symbol HUD, strength and dexterity would only appear when in the melee or ranged fighting mode. Mana and Psi Power would only appear when in the respective magic casting mode. 
Just the Health was decided to be displayed at all times for reasons unknown. Thus, other than the Health Symbols / Bar, the HUD was hidden completely and only shown when needed.  

The inventory was also hidden by default and could be toggled on or off; which, while being a standard today, was not the default in classical rpgs. By displaying items in the inventory as 3D models just as they are actually found in the game - instead of using abstract pictograms as most games do - another step was done to reduce unnecessary abstractions.  

While both HUD designs managed to *represent* those stats of the player and to simplify this representation to the bare minimum, they remained abstract and reveal a lack of visualisation.  


#### Overcoming the HUD

As said before, the need for the HUD arises primarily in order to display and inform about the changes of Attributes like Life (HP), Mana (MP) and Willpower (WP). In order to overcome this need one would have to find ways to visualise these changes. At least seeds of this idea were already present in the Alpha.  

![Wounded Overlay in v0.64b](/_img/mechanics/visualisation/overlay_wounded.gif)

In v0.64b, if you are injured, the player character stands and walks with an extra animation overlay, slowly hobbling, pressing his hands on his wounds as if to stop the bleeding; combined with visual bleeding effects and sound design to intensify the pressure as the HP of the player decrease, this solution would have made the health bar redundant.  
It was not implemented in the end, be it by lack of time or by deliberate decision, but based on what we know and described so far, it would have been the next logical step, following the vision of radical visualisation they initially proposed and promoted.  


<div class="authorship">
    <img src="/_img/authors/flosha-sm.png" alt="Flosha">
    <p>
        <strong>Author:</strong> Flosha<br>  
        <em>Creative Director</em><br>  
        <br>
        <strong>Written:</strong> 30.12.18 - 27.12.20<br>  
        <strong>Rewritten:</strong> 03.11.22 - 04.12.22  
    </p>
</div>
