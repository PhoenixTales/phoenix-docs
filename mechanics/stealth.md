# Stealth Mode

```
Author:  Flosha
Created: 14.02.2022
Last update: 27.09.2024
```
{: .info }


*05.01.2024*

* Stealth Mode is activated by toggling sneaking at any moment
* as soon as the player enters stealth mode there should be a noticeable audio-visual shift to represent the characters focus, attention and awareness of danger. 
   * Music either fades out or is replaced by a heavily depressed, simplified version with lower volume, e.g. drowning and a bit of percussion only; ideally we could switch between these two seemlessly.
   * The volume of the players own foot step sounds, dependent on the material stepped upon, is heavily increased, as well as the volume of npc voices and other ambient sounds, in order to represent the characters raised awareness of his environment.
   
The sound design in THIEF is very similar to this, just that there it is always like that, while in PHOENIX it is our goal to link it to the Stealth Mode and implement it in a way, that the player is very clearly able to perceive the audio-visual change by entering the stealth mode; this way in that the player pushes a button with the intention of doing stealthy stuff, his intention is met by a transition into a clearly more "dangerous", more intimidating, audio-visual environment, that is meant to complement and represent the player (character) "being on his toes", alert and ready to react. 
{: .subtext }


**Slow vs. Fast Stealth:**  
Similar to Splinter Cell the movement speed needs to be seemlessly scalable from sneaking very slowly to running fast. Stealth characters can both be versatile in slow stealth (which means gameplay in the style of *Thief*) as well as in fast stealth, e.g. for evasion (which would be gameplay in the style of *Assassins*).


## Stealth Perceptions

*14.02.2022*

In order to realise the thief gameplay, we not only have to realise the specific thief skills that were planned for the Alpha, we also have to improve upon the perceptions of the AI in relation to Light, Sound and Smell. 

**Light:** We need a perception of light and darkness that NPCs can react to and that the player can clearly understand. We may do so by checking for lightsources and the range of the corresponding lightvobs to calculate the players visibility, that we then visualise for the player in form of a visibility-bar that shows how hidden/visible he is (see [Stealth HUD](#stealth-hud)). We also have to enable the player to destroy lightsources (distinguish fire etc.) in order to decrease his visibility. 

**Sound:** We have to modify the sound in stealth mode during run-time: The footsteps, causing different sound effects depending on the material walked upon, have to become louder, while the music and other sound effects, with the exception of nearby NPCs, have to become quieter, to show the selective perception of the thief and to represent his focus on the noise that he makes and tries to diminish. For the thief to deal with enemies, he has to be able to distract them (by throwing objects, making sounds) and to get rid of them in silent ways: Knock-out, strangle and/or backstabbing, as well as dragging or carrying their bodies to hide them. 

**Smell:** Not just for animals it is feasable to include smell as an additional sense which the thief can interfere with to deal with enemies. He will be able to distract animals via smell with food that they find to lure them away or into a trap. He can use the same mechanics to slowly tame animals if he learned that skill (not exclusive for thieves). But he also can set something aflame to let someone sense the smell of burning, or he can place something rotten nearby to distract a guard. 


## Stealth Skills

*14.02.2022*

In the Alpha there were nine skills specifically planned for the Thief:

(1) Sneaking  
(2) Hide in Shadows  
(3) Lockpicking (I-III)  
(4) Pickpocketing (I-III)  
(5) Sixth/Seventh Sense  
(6) Acrobatics [+ II-III]  
(7) Dirty Daggertricks (I-III)  
(8) Dark Sense (Nightsight) &    
(9) Assassination  


### Skill Description

*06.09.2024 - 27.09.2024*

* **Sneaking** is possible while being upright as well as being crouched or lying/crawling and thus independent from position. This is not only done because it is more believable - since it is easy to move silently while upright and surely does not require a crouched position, but it also helps to lay more emphasis on the new, primary audio-visual changes of the stealth mode. Toggling stealth mode does not mean crouching down, it just means starting to move carefully, more silently and raising the awareness of the surroundings. The player needs to be able to crouch down independently of the sneaking to hide behind objects.

* **Stealing** is possible by approaching an npc from behind or by approaching a sleeping or unconscious NPC, while in stealth mode; initiated by the `ACTION` key instead of speaking to him as in exploration mode (while NPCs in FollowMode are still regularly speakable to during stealth). *Only* when the NPC is sleeping or unconscious the inventory of the NPC opens, signifying that the player searches through the pouches of the NPC; the player can *never* access the inventory of a conscious NPC, he can only steal an item directly that the NPC e.g. carries at his belt (for instance he may carry a key or a pouch with silver directly, it can be stolen from him in the same way as in Thief).

* **Lockpicking**, mostly related to crates and doors. Different locks may require different tools. The camera should focus on the lock and the lockpicks, the lockpicking itself should occur by moving into *four* directions (instead of the original two) by *sensing* (combined with *hearing*) which direction can be pushed into; no direct minigame where the internal lock is seen, but an indirect and more realistic way. But the details of the mechanics can only be clarified after research of different ancient and medieval locks has been done, which may function very differently and may require different techniques and tools. 

* **Dark Sense** is a skill from the Alpha. In Phoenix it is not activated by itself in Stealth mode, but is an ability that can be activated by the player, limited by the focus bar. It serves a similar purpose as the night vision + thermal imaging in Splinter Cell (with a bit of a wall hack). When activated, the gamma may be increased and there is a red, bloody silhouette or a similar visual effect around organisms.

* **Hide in Shadows**, another Alpha skill. Has to be activated by the player too, it reduces the visibility of the character by a high percentage. Without this ability, it is still useful for the character to stay in shadows and keep the visibility meter low, but NPCs will not be as short sighted as they are in Splinter Cell or Thief, it will not be possible to remain invisible while staying in a very dark corner while an NPC walks directly past you; no matter how dark the corner, if an NPC reaches a specific distance of like e.g. 5 meters while directly looking into the players direction, he *will* sense him. Therefore it is important to stay behind them or properly *hide*, e.g. in a barrell, behind a cover, under a bed... the shadows alone do not suffice, unless you activate *Hide in Shadows* which works like a short magically induced invisibility; only this way you can remain actually invisible as long as you are in a dark shadow even if a guard comes close, but only for a short time; otherwise this is not the kind of stealth we aim for. Ideally we would visualise this by the character completely wrapping himself into his black cloak.  

* **Sixth/Seventh Sense**, also an Alpha skill, sometimes referred to as the "Sixth" sense, sometimes as a "Seventh" sense. I do not know what it was meant to be, but we will do further research and thinking. Due to both of these terms appearing in the Alpha (sixth/seventh) we also could use this by having a "seventh" sense as an upgrade to the "sixth" sense skill. 

* **Acrobatics**: Other than sneaking around, opening closed doors and chests (picklock), stealing from a sleeping guard (pickpocket) and killing silently (assassination) with a dagger, all while having a heightened awareness (seventhsense/darksense), there is another important ability of the gothican Thief: his agility. He has to be more agile than any other class. He must reach windows, roofs, all kinds of places inaccessible to other classes. Thus, what we want for the thief class is to link the cross-class *Climbing* skill (it was meant to be learnable in the Alpha) to the thief-exclusive Acrobatics (in form of Lev 2-3) in order to enable him to become sort of a traceur (parcour). This is a crucial aspect of a thief, in German called "Fassadenkletterer" (which in English is called *cat burglar* - in the Comic Diego is seen doing just that). And when he is on the run, he has to be able to use his surroundings to his advantage, be it by destroying something and blocking the way for his persecutors, by fleeing over the roofs, by hiding in a barrell etc. 


## Stealth Hud

Entering Stealth mode toggles the Stealth Meter as well as the Focus Bar. The Stealth meter shows his visibility or how much he is hidden, while the focus bar can be seen as the thieves ability to fully concentrate, or as some sort of "luck" or as a "prayer to Beliar" to hide him in the shadows or as whatever the player may think of it; different NPCs will describe it in different ways, thereby giving an abstract game mechanics a concrete ingame background. 

* **BarHUD:** Visibility is represented by a visibility bar in dark blue - maybe with sprinkles of gold like stars - with a light/golden colour fade, where more ofdark blue means being more hidden, more gold means being more visible. It appears in the right lower corner of the screen (where the mana and psi bar appear for the mage and psionic).  
The focus bar may appear in the lower centre of the screen, where otherwise the endurance bar appears. It also could be displayed in a different way than the other bars (e.g. vertical, also because it is a class-crossing idea) or may be ommitted altogether and may thus work by visualisation only. 

* **IconHUD:** Instead of the bar, visibility is here represented by crescent moon icons that appear on the left bottom corner below the hitpoints (instead of the mana/psi icons for the other classes); the moons show varying degrees of light from left to right. The display of the Focus (if there is any) has to be clarified.

* **NoHUD:** When playing with no HUD, the player needs to develop a feeling for visibility on his own and needs to use his thief skills most effectively; in lack of a visible focus bar we need to work with audio-visual cues, such as a clear, non-obtrusive sound effect that is clearly fading out when the focus is depleted. 


<style>
    main {
        background: url("/_img/bg/code.jpg");
        background-position: top right;
        background-size: 70%;
        background-repeat: no-repeat;
        width: 100%;
    }
</style>
