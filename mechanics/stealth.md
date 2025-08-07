# Stealth Mode

```
Author:  Flosha
Created: 14.02.2022
Last update: 01.10.2024
```
{: .info }


*05.01.2024*

* Stealth Mode is activated by toggling sneaking at any moment.
* As soon as the player enters stealth mode there should be a noticeable audio-visual shift to represent the characters focus, attention and awareness of danger. 
   * Music either fades out or is replaced by a heavily depressed, simplified version with lower volume, e.g. drowning and a bit of percussion only; ideally we could switch between these two seemlessly.
   * The volume of the players own foot step sounds, dependent on the material stepped upon, is heavily increased, as well as the volume of NPC voices and other ambient sounds, in order to represent the characters raised awareness of his environment.
   
The sound design in THIEF is very similar to this, just that there it is always like that, while in PHOENIX it is our goal to link it to the Stealth Mode and implement it in a way, that the player is very clearly able to perceive the audio-visual change by entering the Stealth Mode; this way in that the player pushes a button with the intention of doing stealthy stuff, his intention is met by a transition into a clearly more "dangerous", more intimidating, audio-visual environment, that is meant to complement and represent the player (character) "being on his toes", alert and ready to react. 
{: .subtext }


**Slow vs. Fast Stealth:**
Similar to Splinter Cell the movement speed needs to be seemlessly scalable from sneaking very slowly to running fast. Stealth characters can both be versatile in slow stealth (which means gameplay in the style of *Thief*) as well as in fast stealth, e.g. for evasion (which would be gameplay in the style of *Assassins*).

<!-- TOC_PLACEHOLDER -->

## Stealth Perceptions

*14.02.2022*

In order to realise the thief gameplay, we not only have to realise the specific thief skills that were planned for the Alpha, we also have to improve upon the perceptions of the AI in relation to Light, Sound and Smell. 

**Light:** We need a perception of light and darkness that NPCs can react to and that the player can clearly understand. In the Alpha it was planned to distinguish visibility only via three different factors of illumination: (1) fully illuminated by a lightsource, (2) partially in shadows: semi-darkness and (3) no illumination: darkness.
We may either do it accordingly, or depending on our light system we may do it more granulary by checking for lightsources and the range of the corresponding lightvobs to calculate the players visibility, that we then visualise for the player in form of a visibility-bar that shows how hidden/visible he is (see [Stealth HUD](#stealth-hud)). We also have to enable the player to destroy lightsources (extinguish fire etc.) in order to decrease his visibility. 

**Sound:** We have to modify the sound in stealth mode during run-time: The footsteps, causing different sound effects depending on the material walked upon, have to become louder, while the music and other sound effects, with the exception of nearby NPCs, have to become quieter, to show the selective perception of the thief and to represent his focus on the noise that he makes and tries to diminish. For the thief to deal with enemies, he has to be able to distract them (by throwing objects, making sounds) and to get rid of them in silent ways: Knock-out, strangle and/or backstabbing, as well as dragging or carrying their bodies to hide them. 

**Smell:** Not just for animals it is feasable to include smell as an additional sense which the thief can interfere with to deal with enemies. He will be able to distract animals via smell with food that they find to lure them away or into a trap. He can use the same mechanics to slowly tame animals if he learned that skill (not exclusive for thieves). But he also can set something aflame to let someone sense the smell of burning, or he can place something rotten nearby to distract a guard. 


## Stealth Skills

*14.02.2022*

In the Alpha there were nine skills specifically planned for the thief. Nine skills in the art of thievery (Diebeskunst). They were also summarised in skill overview tables as "List-Talente" (Cunning-Skills, opposed to e.g. *Kampf-Talente* - Combat-Skills):

(1) Sneaking
(2) Pickpocketing (I-III)
(3) Lockpicking (I-III)
(4) Hide in Shadows
(5) Disarm Traps
(6) Acrobatics [+ II-III]
(7) Dirty Daggertricks (I-III)
(8) Sixth/Seventh Sense
(9) Dark Sense (Nightsight)


### Skill Description

*06.09.2024 - 27.09.2024*


#### Sneaking 

Sneaking means moving without causing sound or causing significantly less sound, accompanied by custom sneaking animations. It is possible while being upright as well as being crouched or lying/crawling and thus independent from position. This is not only done because it is more believable - since it is easy to move silently while upright and surely does not require a crouched position, but it also helps to lay more emphasis on the new, primary audio-visual changes of the stealth mode. Toggling stealth mode does not mean crouching down, it just means starting to move carefully, more silently and raising the awareness of the surroundings. The player needs to be able to crouch down independently of the sneaking to hide behind objects.
Some surfaces are harder to move silently on then others. Therefore, depending on the skill of the character, he can move fast silently on some surfaces, while being forced to move very slowly on other surfaces in order to remain silent.


#### Stealing 

Stealing is possible by approaching an npc from behind or by approaching a sleeping or unconscious NPC, while in stealth mode; initiated by the `ACTION` key instead of speaking to him as in exploration mode (while NPCs in FollowMode are still regularly speakable to during stealth). *Only* when the NPC is sleeping or unconscious the inventory of the NPC opens, signifying that the player searches through the pouches of the NPC; the player can *never* access the inventory of a conscious NPC, he can only steal an item directly that the NPC e.g. carries at his belt (for instance he may carry a key or a pouch with silver directly, it can be stolen from him in the same way as in Thief).


#### Lockpicking

Mostly related to crates/chests and doors. Different locks may require different tools. In the Alpha it was planned to let lockpicking always be successful. Later a more interactive system was implemented in which the player needed to move the lockpick left or right by a strict sequence that he had to memorise by trial & error.
In Phoenix, we solve it as follows: The camera focuses closer to the lock and the lockpicks, the lockpicking does then occur by moving into *four* directions (instead of the original two) and not by trial & error but by *sensing* (including *hearing*) which direction can be pushed into: Can it be moved or is there resistance? This requires some sort of careful movement (easier to do on the gamepad). No direct minigame where the internal lock is seen, but an indirect and more realistic approach.
The concept can be developed further after some research of different ancient and medieval locks has been done; since they may function very differently they may require different techniques and tools. 


#### Hide in Shadows

A skill from the alpha, where it was meant to function as follows (translated from *Attributes, Talents, Actions* from 21.07.1999):

*Figure that sneaks in semi-darkness becomes invisible.*
*This skill becomes active automatically. Every lightsource has two ranges. The first range is illuminated by the full light intensity, the second range lies in semi-darkness. Everything beyond that does not contain light of the lightsource.*
*A figure in semi-darkness is still seen by NPCs. In ones own viewport and that of other players the figure in semi-darkness is just displayed in a darkened way (shade).*
*If the figure in semi-darkness has mastered "Hide in Shadows", it has the following effect:*
*NPCs see a sneaking figure in semi-darkness not at all anymore.*
*In the viewport of other players the figure is no longer displayed.*
*In ones own viewport, ones own figure is not only displayed with a shade, but completely black (optical feedback of the talent).*

We divert from this concept by requiring it to be activated (not active automatically when learned). Otherwise it functions more or less as described. Without this ability it is still useful for the character to stay in shadows and keep the visibility meter low, but NPCs will not be as short sighted as they are in Splinter Cell or Thief, it will not be possible to remain invisible while staying even in a very dark corner with no light whatsoever while an NPC walks directly past you; no matter how dark the corner, if an NPC reaches a specific distance of like e.g. 5 meters while directly looking into the players direction, he *will* sense him. Therefore it is important to stay behind them or properly *hide*, e.g. in a barrel, behind a cover etc. The shadows alone do not suffice, unless one activates *Hide in Shadows* which works like a short magically induced invisibility; only this way one can remain actually invisible as long as being in darkness even if a guard comes close, but only for a short time; otherwise this is not the kind of stealth we aim for.
Ideally, instead of displaying the character "completely black", thereby having no ingame explanation for this skill that seems to be magical, we would visualise it by the character wrapping himself into a black cloak, that he would get alongside learning the skill. This way it is not a magical talent of the thief who doesn't have access to magic, but explained by a specific (perhaps magically influenced) fabric. 


#### Disarm Traps 

Was described in the internal design documentation as follows: 
> If the PC opens a crate, chest or door, they may be trapped (usually a simple and spectacular explosion trap). If the PC has mastered this skill, one will just hear a clear "click" when opening the object and the trap will be automatically disarmed.

Could be solved just like this or via a more interesting interaction, if one comes to mind. 


#### Sixth Sense

Also an alpha skill, where it is described as *"a sort of extrasensory perception"* by which one can *"recognise things, which one usually cannot perceive"*. An *"automatic discovery of traps, secret doors, invisibile stuff and disguise"* that was meant to work *"in a 3m radius"*.
So by acquiring the Sixth Sense, the player should recognise *traps* (as described above), secret doors (e.g. hidden entries designed for the thief), invisible stuff (for instance other thieves hiding in shadows?) and even "disguise" (that means he would be able to recognise if an NPC or another player is a spy in disguise). The Alpha documents do not describe in which way these things he recognises would look like in the viewport. It could be a sort of aura or red silhouettes.
As with hide in shadows we require to activate the Sixth Sense instead of it being turned on automatically all the time, to facilitate the player to particularly think of it and apply it during exploration.


##### Seventh Sense

In the sources the same skill is sometimes referred to as the "Sixth" Sense and sometimes as a "Seventh" Sense, which most likely was just done by accidents, as these two terms are often mixed up. But due to both of these terms appearing in the Alpha we could use this by adding a "Seventh" Sense as an additional skill.


#### Dark Sense

Also a skill from the alpha, it serves a similar purpose as the night vision in Splinter Cell. It was described to work as follows:
> *A player character with this talent simply receives an additional illumination by which he can look into dark corridors much simpler. The effectiveness in case of an absolutely dark dungeon should clearly exceed the brightness of the brightest lamp.*

At another place they mentioned another important detail, it *"works like a strong torch, but only for the viewport of the talented"*. It is like the equivalent of a light spell for the thief, but only visible to the thief himself, not to any other NPC, as it is no external light source but just his "Dark Sense". This too was meant to work automatically (without activation), which - again - we change, since having a strong illumination (brighter than any lamp) around ones player character all the time does not sound very pleasant. In case of Phoenix, just as *Sixth Sense* and *Hide in Shadows* it is an ability that can be activated by the player and is limited by the focus bar. 

Due to the nature of the skill as basically an improvement of the characters vision (as if being able to see like some animals), we could divide the Dark Sense into two levels. Level 1 is described above, while level 2 would be focused on an improvement of the characters sense of hearing. 
Dark Sense Level 1 enables him to see what usually cannot be seen due to darkness; it lightens up his sense of sight. Level 2 enables him to hear what usually cannot be heard; it lightens up his sense of hearing. 

It develops the regular sound perception of the stealth mode further in that it amplifies NPC noices, making them louder and much more recognisable, while dampening ambient sounds even more than it is the case in stealth mode, while music turns completely off; the player would then be able to hear rustling grass, sniffing animals and monsters even when they are more or less far away.

By increasing the Gamma, the improved hearing could come with a visual disadvantage. It makes sense to only use it for a specific purpose and thereby we show how in order to use his Ear and focus on the sounds, his other senses have to be suppressed to some degree. 


#### Dirty Daggertricks I-III

``TODO``


##### Assassination

``TODO``

A "subskill" among the Dirty Daggertricks.
Requirements: Sneaking, Daggertricks Level 1


#### Acrobatics

Other than sneaking around, opening closed doors and chests (picklock), stealing from a sleeping guard (Pickpocket) and killing silently (Assassination) with a dagger, all while having a heightened awareness (Sixth Sense / Dark Sense), there is another important ability of the gothic thief: his agility. He has to be more agile than any other class. He must reach windows, roofs, all kinds of places inaccessible to other classes. Thus, what we want for the thief class is to link the cross-class *Climbing* skill (it was meant to be learnable in the Alpha) to the thief-exclusive Acrobatics (in form of Level 2-3) in order to enable him to become sort of a traceur (parcour). This is a crucial aspect of a thief, in German called "Fassadenkletterer" (which in English is called *cat burglar* - in the Comic Diego is seen doing just that). And when he is on the run, he has to be able to use his surroundings to his advantage, be it by destroying something and blocking the way for his persecutors, by fleeing over the roofs, by hiding in a barrel etc. 


## Stealth Hud

Entering Stealth Mode toggles the Stealth Meter as well as the Focus Bar. The Stealth Meter shows his visibility or how much he is hidden, while the focus bar can be seen as the thieves' ability to fully concentrate, or as some sort of "luck" or as a "prayer to Beliar" to hide him in the shadows or as whatever the player may think of it; different NPCs will describe it in different ways, thereby giving an abstract game mechanics a concrete ingame background. 

* **BarHUD:** Visibility is represented by a visibility bar in dark blue - maybe with sprinkles of gold like stars - with a light/golden colour fade, where more of dark blue means being more hidden, more gold means being more visible. It appears in the right lower corner of the screen (where the Mana and Psi bar appear for the Mage and Psionic).
The focus bar may appear in the lower centre of the screen, where otherwise the endurance bar appears. It also could be displayed in a different way than the other bars (e.g. vertical, also because it is a class-crossing idea) or may be omitted altogether and may thus work by visualisation only. 

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
