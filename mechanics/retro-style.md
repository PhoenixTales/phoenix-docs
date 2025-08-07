# RetroStyle

```
Author:  Flosha  
Created: 21.08.2024  
Update:  01.09.2024  
```
{: .info }

In the settings under the "Style" category we offer two collections of presets which set specific options. Those preset collections are called `RetroStyle` and `HardcoreImmersion`. 
All the options in question can also be set independently and combined differently, the player should be able to change single aspects to fine-tune, as they may prefer a mixture of some retro features and some immersive features. `RetroStyle` sets the following options: 

* IconHud
* Pixelation (factor 4)
* Texture Warping (maybe, mild)
* [RetroLoot](#retroloot)
* [RetroPrints](#retroprints)


## RetroLoot

The standard option is `ImmersiveLoot`, where all items remain carefully placed by hand at their respective position and are taken by accompanying animations.

`RetroLoot` is an option I want to give, which does the following: 
* All freely placed items in the world (no shop items) are transformed into a `FloatingItem`; floating a bit above the ground. They may or may not also slowly rotate around 360° like in the inventory or this may be reserved for special items, e.g. `MissionItem`.
* A `FloatingItem` is surrounded by a slight light effect; effect style and/or colour may depend on category (e.g. healing potions omit red light etc.)
* While in this `FloatingState` they may be increased in size by a factor of like ~1.2 to 2.0 to create a look similar to titles such as Quake or McGee's Alice.
* All animations related to looting are removed; floating items are taken by walking through them; to this end their collision is removed until taken.
* Containers (chests, crates, npcs etc.) are looted as usual by pressing `ACTION + ↑` when in focus, upon which the containers inventory appears.
* When inventory full (weight-wise or slot/capacity-wise), floating items cannot be taken; this should be made visible to the player by modifying the items visuals (e.g. grey out).
* When an item is dropped out of the inventory, it should behave the same. 
* But this has implications for the distraction feature (when throwing an object). It could be solved as follows: As soon as taken into the hand to throw let the item behave normally with collision (to get sound of impact etc.); then after it hits the ground and stops moving, it transitions into the floating state; as RetroLoot is more a gimmick than a feature, it does no harm if it seems a bit clunky. 


## RetroPrints

In general, we aim to ideally omit prints if possible, we do so via the HUD. 
* In the `IconHUD`, when acquiring a bonus, the HUD will pop-up (if not there already) and show how an additional icon appears and slightly flashes up, accompanied by a sfx; this way the player is informed of all increases in strength, protection, mana, psi-energy etc.
* In the `BarHUD` the same should happen with the bar, as described by Mike in an early handwritten document, the bar flashes up and shows a new maximal increase in width.  

With the `NoPrints` option (standard in `HardcoreImmersion`) we try to visualise everything. But when playing with `NoPrints` *and* without the HUD, the question arises how and if to inform the player of particular events or changes in the game. 
Which we solve differently depending on the case: 
* When a secret is found, an sfx suffices.  
* What if a new Chapter starts?
* When getting a Boni: A specific boni sfx? 
* Game Over does not have to be shown, as death makes it obvious.
We can always make exceptions and either show the HUD or simple prints at the top of the screen or at a corner inspite of the `NoHUD` option so that no relevent information is lost. 

Now, `RetroPrints` on the other hand is specifically embracing prints as in our testing builds; here texts like "Secret found", "Chapter 2" or "Game Over", as well as boni like "+5 Arcane" are printed extra visible in a big font and in the center of the screen in the style of oldschool FPS titles.

Between `NoPrints` and `RetroPrints` we give `SimplePrints` as a third option, to offer less obtrusive text in a smaller font at the top of the screen or at a corner.


<style>
    main {
        background: url("/_img/bg/code.jpg");
        background-position: top right;
        background-size: 70%;
        background-repeat: no-repeat;
        width: 100%;
    }
</style>
