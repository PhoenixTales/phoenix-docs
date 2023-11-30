# World Evolution

**Author:** Flosha
**Written:** 03.11.2023



## Level Structure

One of the earliest summaries of the levels of the game world were written on an early Psi Camp sketch by Mike as a suggestion for internal shortcuts:

```
[AL] [NL] [ST] [FM]
[AM] [VM] [Hö] [OH]
[AT] [DW]
+ 
[OW]
```

We can summarise this list as follows:
The first line lists the four camps at the *overworld*.
The second and third line summarise the *underworld*;
where the second are the underground mines and caves,
while the third are the parts of the underworld, where
reality begins to be diffused with the *otherworld*. 
The fourth is the *overworld* surrounding the camps.
Beyond it all, not mentioned here, the *outside world*. 

The shortcuts mean and translate as follows:

```
AL | Altes Lager      OC | Old Camp 
NL | Neues Lager      NC | New Camp
ST | Sektentempel     ST | Sect Temple
FM | Freie Mine       FM | Free Mine

AM | Alte Mine        OM | Old Mine
VM | Verlassene Mine  AM | Abandoned Mine
Hö | (Natürl.) Höhlen -- | (Natural) Caves
OH | Orkhöhlen        -- | Orc Caves

AT | Alter Tempel     AT | Ancient Temple
DW | Dämonenwelt      DW | Demonworld

OW | Oberwelt         -- | Surface
AW | Außenwelt        OW | Outside World
```

These shortcuts sometimes led to some confusion also among the original team, as in the beginning only the german shortcuts were used and the english shortcuts were introduced much later. Some earlier levels did never receive an english shortcut. For instance, "AM" is the Old Mine in German, but the Abandoned Mine in English. "OW" is the "Surface" in German, but the "Outside World" in English. 

Please take into account, that the Free Mine, even if called "Mine" here, is listed as one of the camps. This is not a mistake. It was also called "Freies Lager" (Free Camp) in the earliest concepts (short FL, or in english FC) and the level (the .zen) is still called "Free Mine Camp" (with waypoints named "FMC") to seperate it from the "Free Mine" dungeon. 

All the other locations known from the game, such as the Old Fort, the Stone Circle or the Troll Canyon and other landmarks like these are not conceptualised as levels themselves, they are part of the general "surface". This is consistent with the actual level structure in the game data, where all the camps, all the mines, dungeons and the surface are seperate .zen files; although the surface is then merged with the four camps to a "world.zen".

----

The next relevant document is the Phoenix Levelstructure concept. It goes into more detail of how the levels are interconnected and lists different sections within dungeons.

```   


                    ___                       /\           /\                                                  /_\
                  _/___/_ ___                 ||   _/|_ __ ||                                            _____ \_/ ___   
                _|_|   |_|\__\_      _/`-_    ||_/|__|_|__\||       _/--_                                |  | |/ \ | |
_||_||_||_||___|__|___|___|__|_|____/_(_)_\___|_____(|)_____|______/_(_)_\______||__         __||______||||||||||||||||||_
    Stone            New              Old           Old           Abandoned       \_|_     _|_/               Sect
    Circle           Camp             Mine          Camp             Mine          |__|_ _|__|                Camp
      .                                |                              |             \__   __/
      .                                |                              |              |_|_|_|
      .                              __|                       _______|               Free
      .                             |                         |                        Mine               Rock Clefts
      .                             |                         |                         |                  ↑       ↑
      .                       --------------          -----------------          ---------------           .       .  
      .                       | Old Mine I |          | Aband. Mine I |          | Free Mine I |           .       .
      .                       --------------          -----------------          ---------------           .       .
      .                             |                         |                         |                  .       .
      .                       ---------------         ------------------         ----------------          .       .
      .                       | Old Mine II |         | Aband. Mine II |         | Free Mine II |          .       .
      .                       ---------------         ------------------         ----------------          .       .
      .                                                       |                         |                  .       .
      .                                                       |                         |                  .       .
      .                                                       |                         |                  .       .
      . . . . . . . . . . . . . . . .                  ------------------------------------------          .       .
                                    .                  |               Orc Caves I              |. . . . . .       .
                                    .                  -----------------------------------------                   .
                                    .                                       |                                      .
                                    .                  ------------------------------------------                  .
                                    .                  |               Orc Caves II             |. . . . . . . . . .
                                    .                  ------------------------------------------
                                    .                                       |
                                    .                                       |
      --------------------------------------                                |
      |    Demon World    |  Magic Tunnel  |                                |
      --------------------------------------                                |
                |            .   .   .   .              ----------------------------------------
                |            .   .   .   . . . . . . . .|               Temple I               |   
                |            .   .   .                  ----------------------------------------
                |            .   .   .                                      |
                |            .   .   .                  ----------------------------------------
                |            .   .   . . . . . . . . . .|               Temple II              |
                |            .   .                      ----------------------------------------
                |            .   .                                          |
                |            .   .                      ----------------------------------------
                |            .   . . . . . . . . . . . .|               Temple III             |
                |            .                          ----------------------------------------
                |            .                                              |
                |            .                          ----------------------------------------
                |            . . . . . . . . . . . . .  |                Temple IV             |
                |                                       ----------------------------------------
                |                                                           |
                |                                                           |
                |___________________________________________________________|



```

The basic structure remained the same. 
Please note that the Orc Graveyard was not a part of the original level concept.

---


At this point of the concept, the following locations were planned:

At the Surface:
* Cliff of the Damned & Marketplace
* Old Camp, Free Camp, New Camp, Sect Temple
* Demontower, Old Fort & Stonehenge

Underground & Beyond:
* Abandoned Mine, Old Mine & Free Mine
* Tunnels between the AM, FM and the Caves
* Natural Caves (also "Orc Caves I")
* Orc Caves (also "Orc Caves II", later "Orc City")
* Temple (Level 1-4)
* Demonworld

What was not yet part of the concept:

* Troll Canyon
* Monastery Ruins
* Mountain Fortress
* Orc Graveyard






## Evolution of the Map

At first, we will look at how the layout of the world map (position of camps, forests, the ocean etc.) has changed in course of the conception phase and how these changes have influenced the setting. 


### The Barrier and its Centre

The Old Camp was always positioned right in the centre of the game world (point 0, at the crossing point of the global X and Y axes). This has never been changed. But due to the reduction in size of the south and the north of the world in later alpha versions, the barrier's scale had to be reduced and it was squished into an oval shape (originally it was supposed to be a perfect sphere). While the Old Camp has never been moved, this change of the barrier's extent put it slightly off the centre, if the barrier is seen as the border of the gameworld that it is. It was the Old Camp, originally called the "Midcity", that was drawn first and that was always meant to be in the middle of the world. 

-> In Phoenix, the barrier will be a perfect sphere again and the Old Camp will be right in the centre.


### The Exchange Place and the Cliff of the Damned

What was also clear from the start, was that the Exchange Place, originally called Marketplace, was imagined to be directly in the north. But while on the very first map sketch by Mike, titled "Orpheus Overview", the cliff was directly in the north of the marketplace, with a lake below the cliff, this has been changed in Mikes much more elaborated "Orpheus Overview Map V1". While the marketplace stayed in the very north, the "Cliff of the Damned", as it was called, was not directly north of the marketplace anymore, but east of it. And the water into which the player was supposed to fall from the cliff, which has been drawn as a lake before, was now directly connected with the ocean; it was still between the marketplace and the cliff, but now, like the cliff itself, it was east of the marketplace. The player was not supposed to swim towards the marketplace, but towards the so called northern forest, from which a way would lead him to the abandoned mine south of the marketplace. Alex Wittmanns Story "Sleeper's Ban" was written with this map layout in mind. And also the Gothic Comic suggests being made in accordance with this idea. 

[Include image section of the place from the map]


### Rivers, the Ocean and how they relate to Camps

In Mikes "Orpheus Overview Map V1", there was only one river flowing south of the Old Camp, from the southwest into the east, into the ocean in the eastern middle of the map. 

[include image]

In his next, untitled map sketch, he added a second river north of the Old Camp, flowing from the northwest straight to the northeast into the ocean. 

[include image]

In all the builds of the game, as early as v0.56c, it was this river who originated in the waterfall at the New Camp. But in Mikes original concepts, it was the first river in the south that would be connected with the New Camp. In all three of Mike's early map sketches, the New Camp was drawn in the southwest and the Free Mine was drawn in the northwest. 

[include images]

But this was changed early on, we don't know for which reason. On the concepts by Ralf and also in the earliest world models we know of, it was reversed. The New Camp was from now on in the northwest, and the Free Mine in the southwest. And it was not a mere cosmetic change. 

[include reconstructed map showing this]

According to the earlier concept, the New Camp was always supposed to be close to the Old Fort; at first there were supposed to be fields at the bottom of the Fort with peasants who would work for the Lord (later General Lee) of the New Camp. The Fort was meant to be close to the barrier, very far southwest, not as close to the Old Camp. 

[include image of the Fort position]

A river was flowing through the middle of the fields and this river was ending in the ocean east of the Old Camp, with the Psi Camp being directly in the ocean there in the east. 

[include image with the river and ocean blue]

In Mikes third map sketch the former fields at the foot of the Old Fort have changed to be rice terraces at the foot of the New Camp, but they were still north of the Old Fort, from which you could look down upon them. The water from the terraces would already lead to a waterfall, which would form a small lake and then flow further, again into where the Psi Camp was supposed to be. But originally, as hinted at above, the Psi Camp was situated in the ocean; it had nothing to do with a swamp. It was only now that the swamp was introduced, in Mikes third map sketch. He decided to disconnect the ocean from this new idea of the swamp, drawing a long coast line in the east, north of the Psi Camp. 

Short:

At first there was only one river in the world in the south of the Old Camp which was supposed to be close to the Old Fort and relatively close to the New Camp, with fields between the New Camp and the Fort. Then a second river was added in the north without any direct connection to a camp. The lake in the south was then conceptualised not only as being close to the New Camp, but as coming from a waterfall from within the camp, in which a dam was build that would water the rice terraces which replaced the former idea of the fields. Next the position of the camp was changed from southwest to northwest and the New Camp was from now on thought to be connected with the northern instead of the southern river. It was modeled in connection with the northern river in all versions of the game we know of. 

Then the shape of the southern river was changed, as it had lost its function of being related with watering the fields. It would no longer run from the left (southwest) to the right (southeast), but rather from the middle of the south to the middle of the east. Under the waterfall it came from there was drawn a lake (with a second, more hidden lake connected to it), underneath the cliff, where the Demontower was thought to be. This shape was roughly kept till release, but additional complexity was added by splitting it to form two rivers running along both sides of the Great Forest in the east.  




### Psi Camp 

[image of Mikes early psi camp]

Initially, the Psi Camp was situated in the ocean, described as a "Pfahlstadt" (pile city), all build on piles in the ocean, close to a mountain range that stretched all the way from the South to the east and in the centre of which was the Demontower (an area that was described as "the Cliffs in the Southeast"). 

When Ralf started to draw his concepts for the Psi Camp, it was already based on the Swamp idea. Instead of just being build on platforms in the ocean it was now supposed to be situated in a dark swamp, everywhere surrounded by huge trees, higher than the player would be able to see. 

[Include image]
First it was just a small wooden temple among the trees, connected to the holy stone with a statue of the enlightened with the third eye on his forehead hewn from the stone. 

Hence the name "Sect Temple" that the developers always used as a description of the whole camp, not as a description of a mere building within the camp, since everyone was in the "temple". The actual temple-like building was just the "sanctum", the holiest place of the temple, but the entire camp was conceptualised as this "temple" of the sect. They kept using this term throughout all the different concept phases of the camp until the new term "Psi Camp" came up at some point. 
{: .subtext}

[include image]
Then a bigger wooden fortress around a tree was drawn, with a smaller holy stone. Now with a sleeper idol instead of the Enlightened, also with the third eye on his forehead. A seperate building was added behind the stone, which would later be described as the "Sanctum" ("das Allerheiligste"). 

[include image]
Finally it was developed into seperated little islands instead of it all being one wooden temple complex; the holy stone remained, but was even more simplified; no statue or idol anymore, only the eye as the sign of awakening. The building behind the stone was kept as an idea and was developed further into the [Sanctum]() with a [Crypta]() underneath. 








## Locations V1

* Cliff
* Marketplace
* Midcity ("Liberal" Camp)
* Slave Miners Fort
* Free Miners Fort
* Gladiator Camp
* Mages Camp [in V1a]
* Psi Temple
* Old Mines (x3)
* Demon Tower
* Orc Caves
* Ancient Temple


**Liberal Camp:**
* Center:
    * Wardens House (Mafia)
    * Barracks (Guard)
    * Mages Chapel [in V1b]
* Outer Ring:
    * Slave Diggers
    * Mercenaries + Arena
    * Thieves/Spies
    * Smith, Beggars etc.


## Locations V2

* Old Camp
* New Camp
* Old Fort
* Free Camp
* Psi Camp





## Phoenix Locations


**Before the revolt:**

* Cliff of the Damned
* Exchange Place
* Old Pass

* Prison Castle
* Miners Fort

**Mines:**
* Old Mine
* Free Mine
* Abandoned Mine
* Lost Mine
* Oldest Mine
* [Fogmine]

**Ruins & Landmarks:**
* Orc Temple
* Stonehenge
* Old Temple
* Fogtower
* Demontower
* Hermit's Valley
* [Bergfestung]

**Forests:**
* Alpha Forest  ("AWood" - OC to AM)
* Old Forest    ("OWood" - OC to OM)
* Great Forest  ("GWood" - OC to PSI)
* High Forest   ("HWood" - OC to OCY)
* Demon Forest  ("DWood" - DT to PSI)
* 


* Old Stonehenge
* Cliffs of the Southeast
* Demontower
* Big lake and the island
* Swamp



### Prison Castle

The tower was a part of the prison, where the most dangerous of the criminals were held in isolation. 



