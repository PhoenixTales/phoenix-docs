# Trading

**Author:** *Flosha*  
**Created:** 28.08.2024  
**Updated:** 01.09.2024  

How to make trading more immersive, simpler and more intuitive.


**28.08.2024**

Every trader has to have a stand, if not a complete shop. And everything he sells, apart of very small items, have to be actually placed in the world. Traders present their goods by actual items on the table in front of them.  
In case of a dealer or other npcs who want to give the player a choice between a few items, - e.g. the dealer of a guild providing a "loadout" for a mission - he may actually place the items in front of him first, like the weapons dealer in *Mafia: The City of Lost Heaven*. 

This way we improve the non-immersive default of the base game, where traders do not even have a stand (not even in a fake way by e.g. a stand with a texture showing the goods he sells), and seem to just pull weapons and armours out of their pockets. In our system, every item the trader sells should correspond to an actual item in his shop.  
Obviously the player can try to steal such items, but the irreversible consequences when caught will most often make it more trouble than it's worth, shops with very valuable items are always guarded etc. 

When the player walks to the table the camera focuses on it at a top-down angle. Now the player can switch left and right, up and down between highlighting the items. (They are literally highlighted, lightened up as in Gothic - or if choosen (default in retro mode) by white brackets in the style of Deus Ex or System Shock 2). 

When highlighted for the first time, the NPC says a few words about the item (in case of a trader, he also mentions the price at the end), which replaces a non-diegetic item description. When waiting for ~4-5 seconds on an item, the description is repeated in case that the player forgot relevant information.

Items are selected with the action key, upon which he may be asked once if he is sure he wants to buy them. There may be an option to bargain (further below).

This way we have both an immersive trading and an immersive "mission gear selection" system. It is used for weapons, armours, potions and similar items. For very small items (lockpicks, drugs etc.), or in other words: for all *underhand deals*, where it is believable that the NPCs just take the items out of their pockets, a simple trading dialogue can be used instead and an *underhand* item exchange animation is played. 

---

**01.09.2024**

An alternative and perhaps even simpler solution especially for bigger shops, where there is not just one table in front of the trader but several shelves around the room. Instead of initiating this trading camera by approaching the stand, it could also be solved as follows. 

Every item in a shop receives a specific flag or we solve it via the portalroom assignment, so that every item within the shop-portalroom behaves accordingly. 

When hitting `ACTION + ↑` an item is taken, containers (NPCs/Chests) are looted, Mobs are used. We include a `FocusView` function which is triggered after 1-2 sec of just *holding* the `ACTION` key (in the same way as holding it in combat mode triggers the combat stance) while an instance is in focus. `FocusView` is accompanied by a dedicated camera which moves the view to the right shoulder of the PC and closer to the viewed instance. (Unless he is close to a wall to his right, which the camera should detect and move to the left.)

When `FocusView` is triggered on a regular item (not in a shop), the PC or as well an NPC in FollowMode may make a comment on the item (as well as a moveable object, a corpse he found and so on), similar to the "inspect" function when the item is already in the hands of the character and he is inspecting it closely and mentions what he notices. This may also become an important mechanic for the adventure parts and riddles to get additional information.

But when in a shop, holding the action key on an item triggers the trader's comment alongside the `FocusView` as well as a trading interface. In the interface you will just see the option:
```
Buy [X Ore] <- Your price ->
```

When letting go of the `ACTION` key, the interface closes. 

Instead of navigating through a traders inventory, you will move your character through the trader's shop and we show that the trader is observing you in his shop, comments on the items you are interested in and mentions the price. 

This system is both simple as well as immersive and lets the player feel more in control at any time; whatever happens, he can immediately just release a button and is again in full control of his character, can turn around and leave. 

---

## Bargaining

**28.08.2024**

With the arrow keys left and right you can make suggestions and bargain about the price with more or less success based on respect by the NPC, the players rank etc.

When offering a price which is too low and gets rejected by the trader, his mood should lower and he should be less willing to accept any further offer. He may even raise his basic price (see Morrowind).

Important: If the player has a very high rank, being a firemage or baron, traders in the OC, depending on their rank, in the most extreme cases, may not dare to tell you a price at all and just give it to you without question, while others (e.g. within the castle) may offer it for significantly reduced cost. Similarly, when being a priest and the like: "Für einen Mann Eures Ranges..." The player clearly has to recognise a change in behaviour and different advantages (or disadvantages) depending on his guild and rank while trading. 

