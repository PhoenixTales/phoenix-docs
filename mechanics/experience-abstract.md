# Experience

Abstract of the Experience System of Phoenix  
*Flosha, July 20th, 2026*

## 1. Experience Structure 
The Player Character can not gain any general experience. He can only acquire experience (1) related to one of the four classes or (2) related to one of the secondary professions. 

## 2. Class-related Experience
There are 4 class-related categories of Exp:  
* `EXP_WEAPONRY` (Warrior Exp)  
* `EXP_THIEVERY` (Thief Exp)
* `EXP_ARCANE` (Mage Exp)
* `EXP_PSIONICS` (Psion Exp)

## 3. Class-Crossing Experience
There are secondary categories of experience that are unrelated to any class or related to more than one class (there shouldn't be a fixed number in case that additional categories have to be added in the future): 
* `EXP_ALCHEMY`
* `EXP_METALLURGY`
* `EXP_MARKSMANSHIP`
* `EXP_HUNTSMANSHIP`
* `EXP_PHILOLOGY`
* `EXP_ARMORY`

## 4. Levels of Experience
Progression of Experience works the same as the progression of Attributes. Every category of Experience has 10 levels, represented by one unique term for each level. But internally, there are 100 maximum points (and 0). 
* **Example:** If one is at Lvl 1 of Weaponry he has at least 10 total Exp in this category. As long as he doesn't reach the points required for Lvl 2 he will still be on Lvl 1. When he gains 20 total EXP in Weaponry over time, he reaches Level 2. If he gains 30 total Exp he reaches Level 3.
