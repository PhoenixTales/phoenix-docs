# Attributes 

Abstract of the Attribute System of Phoenix  
*Flosha, August 8th, 2026, V2*

## Structure of Attributes
NPCs have (1) primary attributes, that all NPCs share and (2) secondary or "status" attributes (with a few listed as "tertiary" basically functioning in the same way, but they are explained further below). While the primary attributes are represented in the character sheet in form of clear text terms, "secondary" attributes only appear in form of icons or bars.  

## Primary Attributes 
Could be described as "Verbalised/Immersive Character Stats".  
All NPCs (Humans and Monsters) share the following three primary attributes. They are displayed in the character sheet in clear text form to be referred to by NPCs. Secondary attributes, that are scaled by these primary attributes, are listed under them. On top of these three attributes come the four "EXP" related Attributes or "Arts" (described in `experience-abstract.md`); those are also described in clear text form:   
* `ATR_CONSTITUTION` // "Konstitution" or ones Physical Condition; relates to ones Stamina, Hunger, Thirst, Fatigue, Intoxication (physical health parameters) and Regeneration parameters.  
* `ATR_POWER` // "Kraft", relates to ones Physical Strength which scales hitpoints and damage points (Strength). 
* `ATR_WILL` (related to Mental Strength: Will scales the resistance against PSI (in form of psionic attacks, PSI waves or PSI radiation, which increase Madness) and defines how much PSI Points (`ATR_PSI` & `ATR_PSI_MAX`) an NPC skilled in Psionics (`EXP_PSIONICS`) can maximally have). 

## Secondary Attributes 
Could be described as "Visualised Roleplaying Stats".  
The following attributes also appear in the character sheet for every character, but Mana and Psi are excluded for Non-Mages and Non-Psionics (we may or may not only display them in the character sheet after having learned about them ingame by initiation into a magic circle or the Sect, but for debugging purposes both can be displayed; later in the HUD it will be impossible to display both of them, as one cannot be a Mage and Psionic simultaneously; the PSI bar will be positioned at the same place where otherwise the Mana bar would be; same for the Psi icons instead of the Mana icons). 

* `ATR_HITPOINTS` & `*_MAX` // "Lebenspunkte", Hitpoints or Damage that can be endured. (Icon HUD: Life Icons. Bar HUD: Red Bar; different effects will be applied on the bar when hungry/exhausted/poisoned).
* `ATR_STRENGTH` // "Stärke" (in difference to "Kraft"), related to the damage or maximum physical force output of the character, the damage one can inflict (thus influences Damagepoints, "Schadenspunkte" or "Trefferpunkte"). Strength scales damage to 100% in fist fighting (and for monsters, except for Goblins, Zombies and Skeletons with weapons), 50% in melee combat (the other 50% depends on the weapon) and 0% in ranged combat, where it is the weapon and ammunition alone that define the damage; is has no other correlation with `EXP_WEAPONRY` than this partial influence on the damage dealt with the weapons. Strength is reduced by ×0.5 with decreasing hitpoints (that also means: Strength automatically regenerates to its full force when health is regenerated; this mechanic tries to reward the player when he avoids being hit in combat and is believable insofar as that one simply can't be strong while being heavily injured. This has to be tweakable in the scripts; we need the option that the strength is only affected below 50% of Health, 25% of Health etc. (Icon HUD: Fist Icons. Bar HUD: Only displayed in Character Screen).  
* `ATR_DEXTERITY` // "Geschick", related to Physical Control that influences (maybe the critical hit chances in combat, but definitely influences) the risk of failure in stealth interactions and ranged combat (this is its only correlation with `EXP_Thievery`). Specific levels of dexterity are requisites for learning agility and acrobatic related skills (Icon HUD: Hand Icons. Bar HUD: Only displayed in Character Screen). 
* `ATR_MANA` & `ATR_MANA_MAX` // "Mana", "Magische Kraft" (Icon HUD: Blue Star Icons. Bar HUD: Blue Bar). The maximum amount of Mana that one can acquire/tolerate (otherwise he is intoxicated) depends on ones `EXP_ARCANE`.  
* `ATR_PSI` & `ATR_PSI_MAX` // related to Mental Control in form of Psionic Power gained in the Psi Class (Icon HUD: StoneFace Icons. Bar HUD: Green Bar); referred to ingame by Psionics as their "Willpower" (Willenskraft). The maximum amount that one can caquire/tolerate (otherwise he is getting mad) depends on ones `ATR_WILL`.  
* `ATR_FOCUS` & `ATR_FOCUS_MAX` // Focus, the equivalent of Mana/Psi for the Warrior & Thief Class, enables special moves, special attacks and slow motion (see Focus article); comparable to the bullet time meter in *Max Payne* and *Enter the Matrix* or with the combo string for special tricks in *Pro Skater* (Icon HUD: No icons designed yet. Bar HUD: Orange Bar).   
* `ATR_STAMINA` & `ATR_STAMINA_MAX` // "Ausdauer": Has an extra bar that relates to sprinting and diving and to fighting with medium and heavy armor. The constitution level determines the maximum amount of Stamina that can be gained, and it *is* gained (limited by the constitution) through practice, e.g. running with much weight, sprinting etc. (Icon HUD: Air Bubble Icon. Bar HUD: Yellow Bar). 

## Tertiary Attributes 
Could be described as "Visualised Health/Management Stats".   
* `ATR_HUNGER`, `ATR_THIRST`, `ATR_FATIGUE` & `ATR_INTOXICATION`: Hunger, Thirst and Fatigue aren't affecting Hitpoints in any way, but they affect regeneration parameters (REG_LIFE, REG_STAMINA, REG_MANA, REG_SANITY). Intoxication *does* affect Hitpoints. During any amount of Intoxication every regeneration of HP is stopped completely. Depending on the severity of intoxication, HP is either getting reduced a specific amount or contineously until being fatal if not healed. (Icon HUD: One icon each for the four conditions; yet to be designed. Bar HUD: They will colorise the red HP bar, turning it e.g. into a toxic green, when intoxicated, into a dark red when thirsty (representing the "thickening of blood"); for Hunger and Fatigue I don't know yet). 
* `ATR_MADNESS` & `*_MAX` // "Wahnsinn" or ones Mental Condition, increases by exposure to psionic attacks, PSI waves or PSI radiation, when the value of the exposure is beyond ones treshold of *Will*. As intoxication affects HP, Radiation affects Sanity by slow increasements of Madness; if the radiation is low it may increase madness only to a specific amount, if it is very high it may increase it contineously until being fatal if not healed (Icon HUD: Madness Symbols. Bar HUD: It is represented by a Purple-Black bar (turns more black the more it increases, as a simple color-fade). 

Note: "Radiation" is no attribute, but a value we have later to link to specific global events in the Game World (during Madness Waves) or to specific locations in the world through Trigger Zones set in the Spacer.


## Attribute Levels & Scaling

#### Primary Attribute Levels & Scaling

Primary Attributes always have 10 maximum levels, for all NPCs independent of their species (below them the main arts (see `experience-abstract.md`) should be listed as well):

| Primary Attribute   | Level  | Subpoints |
|---------------------|--------|-----------|
| `ATR_CONSTITUTION`  | 1-10   | 1-100     |
| `ATR_POWER`         | 1-10   | 1-100     |
| `ATR_WILL`          | 1-10   | 1-100     |

They are never displayed to the player as numerical values. Each level is represented by a descriptive term, but internally the 10 levels are linked to a maximum of 100 "points". 10 points per level. E.g. below 10 the character is at lvl 0. If he reaches 10 points until 19 he is at lvl 1, 20 to 29 at lvl 2 and so on.  
This is how it should look like in the scripts, at the example of ATR_WILL, with examples of how NPCs may refer to it:  
```
CONST INT MAX_TXT_ATR = 10;

CONST STRING TXT_ATR_WILL [MAX_TXT_ATR] = {
	"besessen", // You are possessed.
	"keinen", // You have no willpower at all. // Willenlos.  
	"schwach", // Your willpower is weak! // Du bist willensschwach.  
	"flüchtig", // Your will is fleeting. 
	"zaghaft", // Your will is craven. 
	"gefestigt", // Your will is stable.. 
	"stark", // Your will is strong.
	"unbeugsam", // You have an unyielding will. 
	"eisern", // You have an iron will. 
	"frei" // You have attained free will. 
}
```

A full WIP table of the primary attributes is given below (it includes the "arts" / categories of experience as well):

| Points | Kraft          | Konstitution     | Wille          | Waffenkunst   | Diebeskunst    | Arkane Gabe | Psionik      |
|--------|----------------|------------------|----------------|---------------|----------------|-------------|--------------|
| 0-9    | gelähmt        | halbtot          | besessen       | keine         | keine          | keine       | narkotisch   |
| 10-19  | schwindsüchtig | komatisch        | keinen         | wehrlos       | unbeholfen     | Kreis 1     | schlafend    |
| 20-29  | schwächlich    | kränklich        | schwach        | unsicher      | tollpatschig   | Kreis 2     | träumend     |
| 30-39  | schwach        | anfällig         | flüchtig       | wehrhaft      | ungeschickt    | Kreis 3     | fantasierend |
| 40-49  | kräftig        | robust           | zaghaft        | treffsicher   | geschickt      | Kreis 4     | eingekehrt   |
| 50-59  | stark          | widerstandsfähig | gefestigt      | sehr behände  | fingerfertig   | Kreis 5     | durchbrochen |
| 60-69  | bärenstark     | athletisch       | stark          | Meister       | meisterhaft    | Kreis 6     | geblendet    |
| 70-79  | unbezwingbar   | zäh wie Leder    | unbeugsam      | ...           | Fingerkünstler | Secret      | versunken    |
| 80-89  | Secret         | Secret           | eisern         | ...           | ...            | Secret      | erleuchtet   |
| 90-100 | Secret         | Secret           | frei           | Schwertsänger | ...            | Secret      | erwacht      |


In the character sheet the Attributes are displayed to the player in form of the attribute name (or an associated image) and the related term of the attribute level he currently is at. For clarities sake and for testing purposes we can additionally show the total points gained in brackets behind. Example:  
```
Wille: unbeugsam (85)
```
The player then knows he is at will lvl 8 (an unyielding will, as teachers will tell him) and has 5 more point boni to gain in order to reach the next level (iron will). 

**Important clarification:**   
Primary Attributes, internally, have a fixed maximum number of 100 points, with always 10 points per level. This gives us more opportunity to reward the player with bonus points, since otherwise we only could give him 10 total boni in total throughout the entire playthrough. These internal points should not be confused with the primary attribute levels or with the points of secondary attributes, therefore we could describe them as "subpoints" as well, while referring to the primary attribute levels as "full points". Subpoints (one of 100) are needed to reach one new "full" point (one of 10 levels). This ONLY applies to the primary attributes: Constitution, Power (Physical Power), Will (Mental Power) and the four Arts (Categories of Experience).  


### Secondary & Tertiary Attribute Levels & Scaling

Secondary Attributes have differing maximum values and are *not* displayed like the primary ones in clear text form, but in form of Icons or Bars only (depending on whether the player has chosen the Icon HUD or Bar HUD in the menu). Range of Values per Species (HUM = Humans, ORC = Orcs, MON = Monsters):  						

| Attributes      | HUM  | ORC   |  MON  |
|-----------------|------|-------|-------|
| `ATR_HITPOINTS` | 5-30 | 15-45 |  ≤100 |
| `ATR_STRENGTH`  | 1-15 | 10-30 |  1-60 |
| `ATR_DEXTERITY` | 1-15 |  1-10 |  1-10 |
| `ATR_MANA`      | 0-30 |     0 |     0 |
| `ATR_PSI`       | 0-30 |  0-50 |  ≤100 |
| `ATR_FOCUS`     | 0-10 |  0-20 |  0-30 |
| `ATR_STAMINA`   | 0-30 |  0-30 |  0-60 |
| `ATR_HUNGER`    | 0-15 |  0-15 |  0-15 |
| `ATR_THIRST`    | 0-15 |  0-15 |  0-15 |
| `ATR_FATIGUE`   | 0-15 |  0-15 |  0-15 |
| `ATR_INTOXATION` | 0-15 |  0-15 |  0-15 |
| `ATR_MADNESS`   | 0-15 |  0-15 |  0-15 |

The values above are meant as a range of values for NPCs that we will manually give the NPCs in the scripts. It does NOT mean that a Human always has 5 `ATR_HITPOINTS`, it only means that 5 is the minimum amount that human NPCs usually have as their `ATR_HITPOINTS_MAX` maximum; the player will also start with 5 HP. But of course one can be injured and get below 5 HP or be dead (0 HP); same for the other values. 

The three health related attributes *Hunger*, *Thirst* and *Fatigue*, are internally consisting of these 0-15 points, but they aren't meant to be displayed like the other values in form of 0-15 icons. Instead they are meant to work like this: At 0 points -> no symbol. Between 1 and 5 points -> a "light" symbol. Between 6 and 10 points -> a "medium" symbol. And between 11 and 15 points -> "heavy" symbol. That means, one is either *not*, or *slightly*, or *moderately*, or *very* hungry/thirsty/tired. Each of these four or three levels affects the regeneration more, slowing it down further or (at "very") stopping it completely. All three values, hunger, thirst and fatigue stay for a fixed amount of time at 0 (because one has eaten food and consumes the energy, is sufficiently hydrated, is sufficiently rested etc.), and only when the energy is depleted, they slowly start to increase from 1 to 15. 

In case of intoxication it is similar in the icon HUD: At 0 intoxiation: No symbol. When someone is slightly intoxicated (e.g. drinking a bit of alcohol) it will be around 1 and 5. When excessively drinking or consuming mana beyond ones arcane knowledge or when poisoned by a monster or a poisoned arrow or whatever else, it will increase similarly in these three levels, with a different symbol for each level. In case of the Bar HUD the intoxication will just be shown by colorising the HP Bar and beginning to deplenish the energy; between 1 and 5 not at all (just stopping any regeneration). Between 6 and 10 it will deplenish the HP slowly and between 11 and 15 it will deplenish the HP fast; the coloration may change in each level, to let it appear more dangerous, it could also later be accompanied by an effect on the bar (e.g. slight pulsating etc.), not to mention animation overlays for the character.

#### Secondary and "tertiary" attributes are ALWAYS integers (whole numbers)

Other than the primary attributes, secondary and tertiary attributes do NOT have the above mentioned subpoints. This makes it much easier to handle technically, since some of those attributes have as much as 100 points (e.g. Health of some Monsters). It also makes it much more clear and consistent for the player.  
* If he receives a message on the screen like "+1 Life gained", then this will immediately and actually be shown as one new Heart Icon (or in our later to be made improved Bar HUD it will be visible through an increased bar size and an unobtrusive visual effect to show this increasement). If he gains "+1 Strength" he will see one more fist icon and so on. Otherwise, if that would not be the case and if it would work like with the primary attributes, players would always be confused, since the apparent increasement is not actually shown and isn't immediately visible; he would then always have to consult the character sheet, which we try to prevent, as our HUD is supposed to give him all the relevant information without a need to check the character sheet.
* This also means: Any enemy, if he attacks and makes any amount of damage, will always at least make one full point of damage. If one has 5 HP points in total, five "full points", and is attacked by a young scavenger which may cause some limited amount of damage, it costs at least one full point in the icon HUD or a fifth of the bar in the bar HUD. In the same way, if one casts a spell that costs mana (scrolls don't), and one may have e.g. six full mana points, any kind of spell will at least cost 1 of these points, there are no half points or something like that; or, in case of the bar HUD, it would reduce at least a sixth of the bar. 

#### Clarification in regard to PSI 
PSI can only be acquired by first gaining the necessary basic psionic experience (`EXP_PSIONIC`) and then by finding PSI knots or consuming PSI drugs with permanent boni. Only characters of the PSI class, Undead Orcish Shamans and the Sleeper have PSI. *Will* determines the maximum level of PSI that one can acquire (otherwise trying to consume more PSI will lead to PSI radiation, leading to Madness); beyond the basic knowledge of PSI, `EXP_PSIONIC` is related to the PSI spells one can learn. 

For the player character, the amount of Will determines the maximum amount of Psi he can *acquire* at that point, as listed below (e.g. with 1 Will he can maximally have 3 Psi, with 2 Will he can maximally have 6 Psi and so on), while non player characters, which belong to the psionic class (one of the three PSI guilds), won't have to acquire the Psi, but when an NPC has 1 Will, we will give him 3 Psi and so on. 

| Will | ≤ Psi |
|------|-------|
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

Human NPCs have a maximum PSI value of 30. For Undead Shamans the maximum PSI value is scaled by factor 1.5. For monsters by factor 2. Thus, the strongest human Psionic (Y'Berion) has 30 PSI, the strongest Undead Shaman has 45 PSI and the Sleeper has 60 Psi. 

**Casting into Madness:** When casting PSI spells they can be continued to be casted even if ones PSI is at zero. If ones PSI is 0, every additional second of casting beyond ones PSI energy, increases ones Madness by one point. PSI spells can be *continued* to be casted with 0 PSI points "into madness", but they cannot *started* to be casted with 0 PSI points. 


#### Clarification in regard to Mana

Similar to PSI, Mana can only be acquired by first gaining the necessary arcane knowledge (`EXP_ARCANE`) and then by consuming Mana potions with permanent boni. The arcane knowledge determines how much Mana can be permanently increased without fatal (physical, mana-induced) intoxication, like the *Will* (and Psionic Knowledge) of a Psionic defines how much PSI can be consumed without fatal madness. 

| Arcane | ≤ Mana |
|--------|--------|
| Lv1    |      3 |
| Lv2    |      6 |
| Lv3    |      9 |
| Lv4    |     12 |
| Lv5    |     15 |
| Lv6    |     18 |
| Lv7    |     21 |
| Lv8    |     24 |
| Lv9    |     27 |
| Lv10   |     30 |

<!---
TODO:
* How to technically include Hunger, Fatigue, Intoxication (physical poisoning) and Radiation (mental poisoning)? Via ATR_* or with some new constants on their own? 
-->
