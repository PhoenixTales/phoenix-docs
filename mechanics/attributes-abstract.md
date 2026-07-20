# Attributes 

Abstract of the Attribute System of Phoenix  
*Flosha, July 20th, 2026*

## Structure of Attributes
NPCs have (1) general attributes, that all NPCs share and (2) special attributes, that are limited to specific species, classes or individuals. Of these general and special attributes, some or "primary" attributes, which are represented in the character sheet in form of clear text terms, while others are "secondary" attributes, which appear only in form of icons or bars.  

## General Attributes
All NPCs (Humans and Monsters) share the following attributes (although different species have different maximum values). General attributes are displayed in the character sheet from the very beginning. They are linked with the secondary attributes listed below them:   
* `ATR_CONSTITUTION` // "Konstitution" or ones Physical Condition; relates to ones maximum endurance. 
  * `ATR_ENDURANCE` 
* `ATR_MADNESS` // "Wahnsinn" or ones Mental Condition. Increases by exposure to psionic attacks, PSI waves or PSI radiation, when the value of the exposure is beyond ones treshold of *Will*. 
* `ATR_STRENGTH` // "Kraft", relates to ones Physical Strength which scales hitpoints and damage/force points. 
  * `HP` // "Lebenspunkte", Hitpoints or Damage that can be endured.
  * `DMG` // "Trefferpunkte", Damage or physical force that can be inflicted (Strength scales damage to 100% in fist fighting, 50% in melee combat (the other 50% depends on the weapon) and 0% in ranged combat - here it is the weapon and ammunition alone that define the damage)  
* `ATR_WILL` (related to Mental Strength: Will scales the resistance against PSI (in form of psionic attacks, PSI waves or PSI radiation) and defines how much PSI Points (`ATR_PSI`) an NPC skilled in Psionics (`EXP_PSIONICS`) can maximally have). 

## Special Attributes
The following attributes are limited to specific species, classes or individuals. They only appear in the character sheet when the character has more than 0 points in them. 
* `ATR_DEXTERITY` // "Geschick", related to Physical Control that influences critical hit chances in combat and risk of failure in stealth interactions. Specific levels of dexterity are requisites for learning agility and acrobatic related skills.
* `ATR_PSI` // related to Mental Control in form of Psionic Power; can only be acquired by gaining psionic experience (`EXP_PSIONIC`) and by finding psi knots or consuming PSI drugs with permanent boni. 
* `ATR_MANA` (


## Secondary Attributes
There are 



## Progression of Primary Attributes 
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

## Display of Primary Attributes 
In the character sheet the Attributes are displayed to the player in form of the attribute name (or an associated image) and the related term of the attribute level he currently is at. For clarities sake and for testing purposes we can additionally show the total points gained in brackets behind. Example:  
```
Wille: unbeugsam (85)
```
The player then knows he is at will lvl 8 (an unyielding will, as teachers will tell him) and has 5 more Willpoints to gain in order to reach the next level (iron will). 

## Progression and Display of Secondary Attributes
Secondary Attributes have differing maximum values and are displayed by Icons or Bars in the character sheet and in the HUD. 

## 2. Attributes of Condition
There are two attributes related to the characters physical and mental condition; these conditions are influenced by different secondary attributes in differing ways:  
* `ATR_CONSTITUTION` (Physical Condition)
* `ATR_SANITY` (Mental Condition)
 
## 3. Attributes of Strength
There are two attributes related to the characters physical and mental strength. These strengths are influenced by different secondary attributes in different ways:  
* `ATR_STRENGTH` (Physical Strength)
* `ATR_WILL` (Mental Strength)

## 3. Attributes of Control
There are two attributes related to the characters physical and mental control:  
* `ATR_DEX` (Physical Control)
* `ATR_PSI` (Mental Control)  


## Relation of Primary and Secondary Attributes

* 


atrributes:
* ATR_Strength
* ATR_Hitpoints
  * ATR_Hitpoints_Max

