# Attributes 

Abstract of the Attribute System of Phoenix  
*Flosha, July 20th, 2026*

## Structure of Attributes
NPCs have (1) general attributes, that all NPCs share and (2) special attributes, that are limited to specific species, classes or individuals. Of these general and special attributes, some or "primary" attributes, which are represented in the character sheet in form of clear text terms, while others are "secondary" attributes, which appear only in form of icons or bars.  

## General Attributes
All NPCs (Humans and Monsters) share the following attributes (although different species have different maximum values). General attributes are displayed in the character sheet from the very beginning. Below are primary attributes; secondary attributes are listed below the primary attributes to which they are linked:   
* `ATR_CONSTITUTION` // "Konstitution" or ones Physical Condition; relates to ones stamina points.  
  * `ATR_STAMINA` & `ATR_STAMINA_MAX` // "Ausdauer": Has an extra bar that relates to sprinting and diving and to fighting with medium and heavy armor
  * `ATR_HUNGER`, `ATR_THIRST` & `ATR_FATIGUE`: They aren't affecting Hitpoints in any way, but they affect regeneration parameters (REG_LIFE, REG_STAMINA, REG_MANA, REG_SANITY).
  * `ATR_INTOXICATION` // Every regeneration of HP is stopped and depending on the severity of intoxication, HP is either getting reduced a specific amount or contineously until being fatal if not healed. 
* `ATR_MADNESS` & `ATR_MADNESS_MAX` // "Wahnsinn" or ones Mental Condition, increases by exposure to psionic attacks, PSI waves or PSI radiation, when the value of the exposure is beyond ones treshold of *Will*.
  * `ATR_RADIATION` // As intoxication affects HP, Radiation affects Sanity by slow increasements of Madness; if the radiation is low it may increase madness only to a specific amount, if it is very high it may increase it contineously until being fatal if not healed. 
* `ATR_STRENGTH` // "Kraft", relates to ones Physical Strength which scales hitpoints and damage/force points. 
  * `HP` // "Lebenspunkte", Hitpoints or Damage that can be endured: `ATR_HITPOINTS` and `ATR_HITPOINTS_MAX`. 
  * `DMG` // "Trefferpunkte", Damage or physical force that can be inflicted.    
* `ATR_WILL` (related to Mental Strength: Will scales the resistance against PSI (in form of psionic attacks, PSI waves or PSI radiation) and defines how much PSI Points (`ATR_PSI`) an NPC skilled in Psionics (`EXP_PSIONICS`) can maximally have). 

## Special Attributes
The following attributes are limited to specific species, classes or individuals. They only appear in the character sheet when the character has more than 0 points in them. 
* `ATR_DEXTERITY` // "Geschick", related to Physical Control that influences critical hit chances in combat and risk of failure in stealth interactions. Specific levels of dexterity are requisites for learning agility and acrobatic related skills.
* `ATR_PSI` // related to Mental Control in form of Psionic Power gained in the Psi Class. 
* `ATR_MANA` // "Mana", "Magische Kraft" 


## Attribute Levels & Scaling

### Primary Attributes

Primary Attributes always have 10 maximum levels (and 0) and are never displayed to the player as numerical values. Each level is represented by a descriptive term, but internally the 10 levels are linked to a maximum of 100 points. 10 points per level. E.g. below 10 the character is at lvl 0. If he reaches 10 points until 19 he is at lvl 1, 20 to 29 at lvl 2 and so on.  
This is how it should look like in the scripts, at the example of ATR_WILL, with examples of how NPCs may refer to it:  
```
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

In the character sheet the Attributes are displayed to the player in form of the attribute name (or an associated image) and the related term of the attribute level he currently is at. For clarities sake and for testing purposes we can additionally show the total points gained in brackets behind. Example:  
```
Wille: unbeugsam (85)
```
The player then knows he is at will lvl 8 (an unyielding will, as teachers will tell him) and has 5 more Willpoints to gain in order to reach the next level (iron will). 


## Secondary Attributes

Secondary Attributes have differing maximum values and are *not* displayed like the primary ones in clear text form, but in form of Icons or Bars only. 


### ATR_CONSTITUTION & ATR_STAMINA

Constitution has 10 levels and a maximum of 100 points. 100 equals lvl 10, 90 equals lvl 9 etc. Stamina has a maximum of 100 points as well. The constitution level determines the maximum amount of Stamina that can be gained. 


### ATR_STRENGTH & ATR_HITPOINTS




### ATR_STRENGTH & DMG



Strength scales damage to 100% in fist fighting, 50% in melee combat (the other 50% depends on the weapon) and 0% in ranged combat (here it is the weapon and ammunition alone that define the damage). 


### ATR_WILL & ATR_PSI

PSI can only be acquired by first gaining the necessary basic psionic experience (`EXP_PSIONIC`) and then by finding psi knots or consuming PSI drugs with permanent boni. Only characters of the PSI class, Undead Orcish Shamans and the Sleeper have PSI. *Will* determines the maximum level of PSI that one can acquire (otherwise trying to consume more PSI will lead to PSI radiation, leading to Madness); beyond the basic knowledge of PSI, `EXP_PSIONIC` is related to the PSI spells one can learn. 

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

Human NPCs have a maximum PSI value of 30. For Undead Shamans the maximum PSI value is scaled by factor 1.5. For monsters by factor 2. Thus, the strongest human Psionic (Y'Berion) has 30 PSI, the strongest Undead Shaman has 45 PSI and the Sleeper has 60 Psi. 

**Casting into Madness:** When casting PSI spells they can be continued to be casted even if ones PSI is at zero. If ones PSI is 0, every additional second of casting beyond ones PSI energy, increases ones Madness by one point. PSI spells can be *continued* to be casted with 0 PSI points "into madness", but they cannot *started* to be casted with 0 PSI points. 


### ATR_MANA 

Similar to PSI, Mana can only be acquired by first gaining the necessary arcane knowledge (`EXP_ARCANE`) and then by consuming Mana potions with permanent boni. The arcane knowledge determines how much Mana can be permanently increased without fatal intoxication, like the *Will* of a Psionic defines how much PSI can be consumed without becoming permanently mad. 


---

TODO:
* How to technically include Hunger, Fatigue, Intoxication (physical poisoning) and Radiation (mental poisoning)? Via ATR_* or with some new constants on their own? 

