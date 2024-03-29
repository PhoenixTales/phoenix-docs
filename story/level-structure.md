# Level Structure

**Author:** Flosha  

**Content:**  

1. [Preface](#preface)
2. [Initial Level Structure](#initial-level-structure-1996-1997)
3. [Early Phoenix Level Structure](#early-phoenix-level-structure-1998-1999)
4. [Later Phoenix Level Structure](#later-phoenix-level-structure-late-2000)
5. [Release Version Level Structure](#release-version-level-structure-2001)
5. [Conclusion](#conclusion)



## Preface 

In this document we are dealing with the abstract level structure. We list every level or level section that was once supposed to be part of the game, describe the interconnection of the underground levels and analyse which levels were added or removed in course of the concept phase and during production.  

What we do not deal with here are the positions of these levels in the game world or how these positions changed (for this read "Evolution of the Map") unless it is about a change in the structure of dungeons which were thereby connected or disconnected, nor do we deal with how those levels were changed in their particular design (which we do in "World Design"). 


## Initial Level Structure (1996-1997)

One of the earliest summaries of the levels of the game world were written on an early Psi Camp sketch by Mike as a suggestion for internal shortcuts, during the Orpheus phase:

```
[AL] [NL] [ST] [FM]
[AM] [VM] [Hö] [OH]
[AT] [DW]
+ 
[OW]
```

We can summarise this list as follows:  
The first line lists the four camps at the *overworld*. The second and third line summarise the *underworld*; where the second are the underground mines and (orc) caves, while the third are the ancient temple and the *demonworld*. The fourth is the *overworld* surrounding the camps. Beyond it all, not mentioned here, the *outside world*.   

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

These shortcuts sometimes led to some confusion even among the original team, as in the beginning only the german shortcuts were used and the english shortcuts were introduced much later. Some earlier levels did never receive an english shortcut. For instance, "AM" is the Old Mine in German, but the Abandoned Mine in English. "OW" is the "Surface" in German, but may be interpreted as the "Outside World" (beyond the barrier) in English. 

Please take into account, that the Free Mine, even if called "Mine" here, is listed as one of the camps. This is not a mistake. It was also called "Freies Lager" (Free Camp) in the earliest concepts (short FL, or in english FC) and the level (.zen) is still called "Free Mine Camp" (with waypoints named "FMC") to seperate it from the "Free Mine" dungeon. 

All the other locations known from the game, such as the Old Fort and other landmarks like this are not conceptualised as levels on their own, as they are part of the general "surface" (therefore we will not deal with them here, where it is about the abstract level structure only). 

This is consistent with the structure in the game data, where all the camps, mines, dungeons and the surface are seperate .zen files that are edited independently; although in the end the surface is merged with the four camps to a "world.zen".


## Early Phoenix Level Structure (1998-1999)

The next relevant document is the [Phoenix Levelstructure concept](https://media.gothicarchive.org/documents/phoenix/PhoenixLevelstruktur.png). It goes into more detail of how the levels are interconnected and lists different sections within dungeons. While most of these dungeons were not yet created at this point, the *concept* presented below was roughly in place from the beginning until v0.6, maybe v0.7 (which was when most world changes at the surface occured; but we cannot say for sure how much the concept of the dungeon structure was changed then). 

<pre class="small">  

                    ___                       /\           /\                                                  /_\
                  _/___/_ ___                 ||   _/|_ __ ||                                            _____ \_/ ___   
                _|_|   |_|\__\_      _/`-_    ||_/|__|_|__\||       _/--_                                |  | |/ \ | |
_||_||_||_||___|__|___|___|__|_|____/_(_)_\___|_____(|)_____|______/_(_)_\______||__         __||______||||||||||||||||||_
    Stone            New              Old           Old           Abandoned       \_|_     _|_/               Sect
    Circle           Camp             Mine          Camp            Mine           |__|_ _|__|                Camp
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
      .                       | Old Mine II | <span class="added">-------</span> | Aband. Mine II | <span class="added">-------</span> | Free Mine II |          .       .
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
                |            .   .   .   . . . . . . . .|                Temple I              |   
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
                |            . . . . . . . . . . . . .  |               Temple IV              |
                |                                       ----------------------------------------
                |                                                           |
                |                                                           |
                |___________________________________________________________|



</pre>

As you can see, the basic structure remained the same. No part of the level as initially imagined during the Orpheus phase was removed from the Phoenix Concept, it rather has been increased in complexity through ideas such as the many sublevels of the dungeons and the temple and by their interconnection. The sublevels of the mines should not be misunderstood to mean that there were additional levels e.g. of the Old Mine in any version of the game; it is more to be seen as a story-related division of one coherent level, where for instance you would only get access to the lower parts of a mine in course of the story. We cannot say the same about the Orc Caves and the Temple for sure, but we know that during development there were no separate levels of the ancient temple that were supposed to be in use simultaneously, there were only different designs at different times replacing the former design. 

At the surface we have the *Old Camp*, *Free Camp*, *New Camp* and the *Psi Camp* (called *Sect Temple* back then) as technically separate levels, while the *Stone Circle* is also specifically mentioned, inspite of technically not being separated from the surface, due to its importance in the story, where it was supposed to serve as the hub of the portals to the different temple areas (which had to be unlocked inside of the temple first, then the corresponding portal had to be activated in the stone circle). 

The *Demontower* turned out to become a separate .zen in the final version, but is not mentioned here; this may either be due to it being conceived as significantly smaller in the Alpha (the later "sunken tower" is just re-using an older model of the Demontower) and thus unproblematic to include directly into the surface; it might as well be due to the idea of the story authors that the Demontower shouldn't be there at all in the beginning and would only have been erected in Chapter 2; or it might be due to the fact that the role of the demon evocator was very unclear and vague in the first story drafts. 
{: .subtext }

Underground & beyond we have the three mines: *Abandoned Mine*, *Old Mine* & *Free Mine* (the latter of which was also sometimes referred to as the "New Mine"). While it was not yet shown on the original abstract above, it is still a very early idea, that the mines should be connected (thus I have added this connection in red). The Abandoned Mine and the Free Mine were always supposed to be linked by a tunnel, which even plays an important role in Alex Wittmann's (once supposed to become official) gothic novel "[Sleeper's Ban](https://gothicarchive.org/documents/SleepersBan.html)".  
But in later documents a connection between the Old Mine and the Orc Caves (perhaps through a connection with the Abandoned Mine) is also hinted at, making them all interconnected. Although the connection from the Old Mine is only ever mentioned in the context of the "lost mine" - e.g. after the mine runs full of water due to the earthquakes during the *Final Prayer*, from which we could deduce, as Dmitriy suggested, that this connection might only open up at this point in course of the (partial) collapse of the mine.

While imagining such a tunnel the reader has to keep in mind that the Free Mine and the Abandoned Mine were originally supposed to be much closer together (much closer even than the Old Mine and the Abandoned Mine in the release version), as one can see on [Mikes Orpheus map](https://media.gothicarchive.org/conceptart/mikehoge/maps/map3.jpg). 
{: .subtext }

It is not sure what the rock clefts towards the Sect Temple were practically supposed to mean, but the swamp was located near to what the documents describe as the "Cliffs in the Southeast", in the middle of which the Demontower was located. The clefts might have been imagined to be between these cliffs and maybe inside the swamp forest too, through which the player could fall (or potentially climb) all the way down to the "Orc Caves". Please note that the *Orc Graveyard* (at the surface) was not a part neither of the initial nor of the early Phoenix level structure. And in the same way there was not supposed to be a simple direct entrance to the underground Orc City at the surface except for these clefts; the regular path into the Orc Caves (or City, as it was later called internally) was through the Mines and Natural Caves.

Thus, at this stage we have the following level structure:

```
[AL] | Old Camp 
[FL] | Free Camp
[NL] | New Camp
[ST] | Sect Temple

[OM] | Old Mine       
[FM] | Free Mine        
[AM] | Abandoned Mine 

Tunnels between AM/FM/OM & Hö/OH
                        
[OH] | Orc Caves I-II        
[AT] | Ancient Temple I-IV

Magical Tunnels between Surface and Temple

[DW] | Demonworld
```


## Later Phoenix Level Structure (late 2000)

But then (corresponding versions v0.7-0.8) the original level structure from the concepts was started to be changed. 

The Orc City level, that is still to be found in the Gothic MDK, was the realisation of at least one of the two before mentioned "Orc Cave" levels (if not both of them; since the Orc City model is thematically divided into natural caves in the beginning and the actual city of the orcs at the end of the level). Thus it is reasonable to assume that the Orc Graveyard was the other of the two. In any way: We can be very sure that the Orc Graveyard was originally meant to be a part of the underground Orc City or a separate level close to or connected to it (and there is a very fitting section in the OrcCity level that seems to lead to nowhere, where the levelchange trigger to the Graveyard could have been).

But now, in opposition to the concepts, when the levels were actually getting implemented into the game world, both the Orc Graveyard and the Orc City became levels to be accessed separately and directly from the surface, instead of through the Mines. This was a dynamic change by which the level designers deviated from the concept during production and it happened as early as v0.8 or even v0.7 (while in v0.6 the levels or any connection to them from other levels did not yet exist or were still in the process of being made, as far as we know). I do not want to say that this change was made against the plannings of the story department, since in this process the story itself was changed too.  

It may not be obvious for some readers how much of a deviation from the initial idea it was. According to the old plan, the player was meant to experience this underworld as a big interconnected cave system with several levels leading him continuously deeper. He was supposed to enter the three mines from the surface, then the deeper areas of the mines, where they transition into unexplored territory, tunnels of monsters, minecrawler lairs; and deeper again he would travel through the natural caves until being confronted by the underground city of Orcs; and from here even deeper he would descend into the unknown, exploring the Ancient Temple, build in different descending levels, with the deepest level being the invocation hall, the sanctum of the Sleeper at the very bottom of the game world; and thus at the bottom of his exploration. 

This was the idea which was discarded for whatever reason. Instead of one connected underground where the exploration of one level gave access to the next deeper level below in a vertical way, now all the levels where presented much more "horizontally", each accessible on its own, except for the Ancient Temple which was still supposed to be accessible only through the underground Orc City.  

While the structure of the levels and their connection changed a lot at this stage, at least the levels themselves that we listed above (except for the connections between the mines) were all still supposed to appear in the game. But not for long.


## Release Version Level Structure (2001)

Now to the release version. Long story short, alongside the extremely simplified story line of the release version, the final level structure was also tremendously reduced: 

* The Abandoned Mine which was so important before, as the connection to the Free Mine and the Orc Caves, was removed completely.
* The Free Mine (which once was playing the biggest part in the story of all the mines) was still there, but narratively it only played a fracture of the role it was supposed to have (which also led them to change the models between Old Mine and Free Mine; the dungeon that players know from the release version as the Old Mine was actually meant to be the Free Mine and vice versa).
* No connection could be realised anymore between any of the mines as well as there was no longer any connection between the mines and the Orc Caves/City.
* The Orc City was completely removed alongside all the story that was supposed to take place there; while little parts of it were recycled in form of a smaller village at the surface, which was by far the biggest of all the cuts in the level structure.
* The Temple could only be made about half as big as imagined (no four levels) with many ideas of both Mike and Ralf being lost and instead of having to open the ancient portal to the temple inside of the underground Orc City, now the access was a dumb gate in the recycled surface village of the orcs.
* The Demonworld could not be realised anymore at all. 


## Conclusion

It should be obvious that our solution for PHOENIX is the return to the initial level structure as it found its most elaborated expression in the early Phoenix Concept shown above. How we will implement this structure in the actual level design and how the game world will change in course of it will be explained in the "World Design" docs. Nothing to change or to add here. 


<div class="authorship">
    <img src="/_img/authors/flosha-sm.png" alt="Flosha">
    <p>
        <strong>Author:</strong> Flosha<br>  
        <em>Creative Director</em><br>  
        <br>
        <strong>Created:</strong> 03.11.2023<br>  
        <strong>Last Change:</strong> 28.03.2024  
    </p>
</div>


## Read next

* Evolution of the Map (wip)



