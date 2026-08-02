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

## 5. Acquisition of Experience

Experience is acquired by...  
1. *specific dialogues* with NPCs (skilled fighters or thieves, mages, psionics, alchemists, hunters etc.) or by reading special books/scrolls (on weapon or combat, on thief skills, on arcane secrets, on alchemy or hunting knowledge etc.), which teach something to the PC that he doesn't yet know. And by...  
2. *application*, both in missions (using weapons/fighting or magic or psionics or thief skills) to solve missions, e.g. +X points for dealing with a particular game situation confronted with during the mission) and also in regular encounters, but then only if the application involves a first-time challenge (e.g. first encounter and kill of a particular monster with a weapon or magic, or first time battle (and win) against an NPC from a particular class and level (e.g. against a templar level 4) or first time forging a particular sword or mining a particular ore (+ metallurgy), or first time casting a particular spell (arcane) or brewing a particular potion (+ alchemy) or taking a specific trophy (+ huntsmanship) and so on. 

This system has the following consequences:  
* There is no point in the story where it wouldn't be to the advantage of the player to keep going forward and solve more story missions, because that is what his character progression depends from → story comes first, the gameplay and mechanics are in accordance with the urgency of the story and there is no possibility of nor any demand for "grinding".
* The player has a strong incentive to use the different special abilities of his class as much as possible and not the abilities of another class, because only by doing so can he progress his character within the chosen class and guild, since e.g. as a mage, any combat experience gained is a missed opportunity to gain magic experience and doesn't let him progress within his chosen role.
* By e.g. constantly choosing means suited to the warrior, while being a thief, he leaves much thievery exp on the table and when doing so consistently he may not only be unable to progress any further within the ranks of his guild and not learn new thief skills (in lack of thievery exp that he needs as a requirement); he may also simply be thrown out of the respective thief guild for being unsuitable for the job, forcing himself to join a warrior guild instead. 
