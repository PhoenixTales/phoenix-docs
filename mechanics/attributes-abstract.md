# Attributes 

Abstract of the Attribute System of Phoenix  
*Flosha, July 20th, 2026*

## Structure of Attributes
NPCs have (1) general attributes, that all NPCs share and (2) special attributes, that are limited to specific species, classes or individuals. 

## General Attributes
All NPCs (Humans and Monsters) share the following attributes (although different species have different maximum values). General attributes are displayed in the character sheet from the very beginning: 
* `ATR_CONSTITUTION` (related to their Physical Condition, which scales their endurance)
  * `ATR_ENDURANCE` 
* `ATR_MADNESS` (related to their Mental Condition)
* `ATR_STRENGTH` (related to their Physical Strength which scales their hitpoints and their damage points). 
  * `ATR_HITPOINTS` (short HP: The Hits/Damage that can be endured)
  * `ATR_DAMAGEPOINTS` (short DP: The Damage that can be inflicted) 
  * 
* `ATR_WILL` (related to their Mental Strength)

## Special Attributes
The following attributes are limited to specific species, classes or individuals. They only appear in the character sheet when the character has more than 0 points in them. 
* `ATR_DEXTERITY` (related to Physical Control)
* `ATR_PSI` (related to Mental Control in form of Psionic Power) 


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

