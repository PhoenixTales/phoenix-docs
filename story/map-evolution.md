# Evolution of the Map 
***Or the Layout of the Overworld***

**Author:** *Flosha*

In the [Level Structure](/story/level-structure) document we analysed the abstract structure of the levels that were supposed to be in the game. Here we deal with the layout of these levels, of the surface or the "overworld" to be more specific (world.zen). We deal with (1) the scope of the barrier (2) the position of camps, forests, rivers, the ocean and important landmarks and (3) how they were moved around in course of development all the way to the final layout.

In the World Design documentation we will "meta-analyse" this evolution of the map, not by analysing one layout of the world after another, as we do here, but by looking at the individual locations specificially as they changed throughout development and speculating about the reasoning behind these changes, before we draw conclusions for our implementation of the overworld in PHOENIX. 

Our findings here will also be important in order to deal with the layout of the underworld in relation to the overworld; or in other words - for the expected position of dungeons in relation to the world above and the interconnection of these dungeons. While this is not of importance in GOTHIC, where there is no interconnection left whatsoever, it will be of importance in PHOENIX, where this interconnection finally finds its way into the game and requires a layout of the dungeons underneath the surface that makes these connections believable. 
{: .subtext}


**Content:**  
1. [Mikes Concepts](#mikes-concepts)
    1. [First Map Sketch](#first-map-sketch)
    2. [Orpheus Map V1](#orpheus-map-v1)
    3. [Last Map Sketch](#last-map-sketch)
2. [Ralfs Concepts](#ralfs-concepts)
3. [V0.7 - V0.9](#v07---v09)
4. [~v0.94 - 1.00](#v094---100)
5. [Sequel Concepts](#sequel-concepts)


## Mikes Concepts

### First Map Sketch

The sketch below is most likely from 1995. It was just a rough draft of a concept in development that was never considered to be "good" or complete as it was, but we mention it nonetheless, since it is part of the evolution from these earliest drafts to the later world map. 

![First Map Sketch by Mike](/_img/story/map/map1.jpg)

The barrier here was drawn just as a line at the northern border of the colony, protecting the cliff as the only way out, to prevent the prisoners from escape (this changed into the idea of a spherical barrier very early on, but not here). The Marketplace was in the very north from the start. 

In the middle of the colony was supposed to be "Midstadt" (Midcity), later the "liberal camp" (as it was called because it was here that the convicts liberated themselves and initiated the revolt; establishing a new rule in the former prison castle and building the "outskirts", the later outer ring of the camp). The Mercenary Camp ("Gladiators" is written under it) is drawn in the southwest, with fields north of it. The Psi Camp was drawn in the northwest, with the idea of some thieves hiding there. And the Free Camp with the free diggers and their mine was in the northwest. 

There was an old mine inbetween Free Camp and Gladiator Camp, not that far away from the Liberal Camp. "Slave diggers" working for the Liberal Camp were drawn in the south (at another mine). The "Abandoned Mine" was not yet specifically mentioned, but we have to point out that according to the early idea there were three "old mines" in the colony. This was not a term that was specifically reserved for one of the mines. That means that what is called "old mine" on the sketch above, is most likely what would later be called the "Abandoned Mine", while what the players know as the "Old Mine" is what is shown here in the south at the position of the slave diggers. 

A very short-lived difference was the mages being situated outside of the camp at a location of their own (the stonehenge and the mages meeting place in the forest may be what was left of it in later (alpha) versions). 

There are two forests, one in the northwest, one very big forest covering almost the entire east. An idea specific to this sketch is the "Half Orcs" being situated in this eastern forest. There was no ocean and no river to be seen (or at least it cannot be perceived anymore, due to the sketches age and decay that we tried to preserve as best as possible) and there was no demontower yet.


### Orpheus Map V1

Somewhere between 1995 and 1996 Mike had conceptualised the world further and developed it into what we can see in his Orpheus "Overview Map" V1. We have to point out that Mike himself called it "V1" since this was the first map he was actually confident about (in opposition to the rough sketch above), which does not mean that he imagined this map to be finished - further improvements and changes were to be expected.

![Map 3 by Mike](/_img/story/map/map2.jpg)

This map sketch was already much more elaborated in that it introduced the ocean, rivers, mountains and so forth. The barrier is now seen as a circle (and please note that Mike has defined the size of the barrier as 1km in diameter here). The marketplace was still in the north. But the cliff of the damned was not anymore north of the marketplace, but east of it and connected directly to the ocean. At this stage of the concept the convicts were not thought to be brought to the marketplace during their conviction. The marketplace and the cliff, while being close together, were seen as two separate things.

The Old Camp (no longer described as the "Liberal Camp" or the even earlier term "Midcity") was still in the very centre of the colony (and thus in the centre of the barrier) with an inner (castle) and an outer ring. The lines you see leading away from the outer ring like sunrays are *not* the trench you may know from the final game, but they are showing the hill that the camp was supposed to be on. At this point in time the Old Camp was supposed to look [like this](https://media.gothicarchive.org/conceptart/mikehoge/locations/alteslager-sketch.png). The mages were now put inside of the camps. The battle mages (as the fire mages were called at the time) were placed inside the Old Camp.

The New Camp was still in the southwest, but the fields were now south of the camp instead of north of the camp and the "Old Fort" appeared in the south of the fields. The healing mages (as the water mages were called) were put inside of the New Camp. A river was introduced flowing through the fields (where peasants were supposed to work for the New Camp) and all the way towards the ocean in the east, towards the Psi Camp. 

The Psi Camp at this point was situated inside of the ocean (not yet in a swamp). It was like a small village on pillars in the ocean close to the shore and was supposed to look [like this](https://media.gothicarchive.org/conceptart/mikehoge/locations/psitemple.png). This is the reason that it was described in Alex' story (in more exaggerated terms) as a "Pfahlstadt" (pile city). 

Mike kept the idea of a forest in the northwest, now stretching a bit further down to the middle of the west, partially surrounding the Free Camp/Mine, which was still in the northwest and was supposed to look [like this](https://media.gothicarchive.org/conceptart/mikehoge/locations/freieslager.png). The Halforcs were moved from the forest to the Free Camp, where they apparently were supposed to live in peace with the free diggers. 

The Abandoned Mine (now described as such and no longer as the "old mine"), was moved from being situated in the west of the Old Camp to the north of the Camp. It was inbetween the Old Camp and the Marketplace and directly on the crossroad between the path from the cliff, from the Marketplace and towards the Old Camp. At this point in time the player was supposed to be thrown down the cliff, swim towards the northern forest (also introduced in this map) and walk through the forest towards the Abandoned Mine and from here to the Old Camp (or the marketplace, if he'd chose to). This is exactly corresponding to the description in Alex Wittmann's story [Sleeper's Ban](https://gothicarchive.org/documents/SleepersBan.html), which was based on this world map and started to be written at this time. The "other" old mine - now actually described as such - remained at the exact same position as before, at the south of the Old Camp. 

Other than that a small forest was introduced at the west of the Old Camp and the Demontower appeared deep inside of the big forest, in an area which was described at this point as "the cliffs in the southeast" which were apparently supposed to be connected with or being part of the forest. It was not supposed to be a very dry and open area, but rather a dark wilderness. 


### Last Map Sketch

For a while we thought that the following map sketch was created before the Orpheus Map V1 above. But actually it is very clear that this sketch was made after V1. The entire layout remained mostly the same, but a few very important changes were introduced. 

![Map 3 by Mike](/_img/story/map/map3.jpg)

The marketplace remained conceptually as before, but the northern lake under the cliff as well as the northern forest were made quite a bit smaller, because a second river was added, running from the northwest towards the sea in the east. The stonecircle was introduced here at a cliff hovering over the sea. Also a pass was drawn in the west (which would lead to freedom, if the barrier wouldn't be in the way). The arrows drawn here at different places on the map are supposed to show how the terrain would lead upwards or downwards. 

It may also be noteworthy that the Old Camp appears to be smaller in relation to the barrier and the game world as a whole. The Old Camp itself was not supposed to be smaller though. But we also have no reason to assume, that the game world itself was supposed to be bigger. In the map V1 the camps were way too close together, there was not enough distance between the camps and if the Old Camp would have been as big as on Map V1 with the same distance to the barrier, the barrier would have been much less than 1km in diameter. Therefore we should see this change only as an adjustment of the *proportions* in the map, not as any actual change in size.  

Otherwise no changes to the Old Camp's position or surroundings, except that the forest in the west of the Old Camp that was introduced before, was now removed and replaced by a very prominent tree. This tree is the first appearance of what later would become the "hangman's tree". 

The New Camp did not change position either. But now the camp is shown in a mountainous area with a waterfall in the west. The river that before was flowing into the sea through the fields south of the New Camp, was now flowing into the camp. The dam is there and the former "regular" fields were replaced by rice terraces directly connected with the camp. Some sort of protective walls (from wood, most likely, very much as in the actual game) were drawn, seeming to protect the camp towards the only two entrances to the fields. One in the north between two mountains, one towards the east. A mountain terrain was added between the New Camp and the Old Camp. 

The Psi Camp, while keeping its position, was actually changed a lot - as well as the surroundings of the camp. For one, a forest was added between the Psi Camp and the Old Camp. But most importantly, the camp was now not anymore supposed to be located inside of the sea, but in a swamp. It is very noteworthy where the coastline is drawn. There was supposed to be a coast north of the Psi Camp roughly in the middle of the map, leading all the way into the east, far beyond the barrier and the view of the player. The actual ocean (we know from documents and early level meshes that it was supposed to be the ocean, not just a lake) was only supposed to be in the *north* and northeast of the Psi Camp - the entire area *east* of the Psi Camp would have been the swamps. And just as the coastline, the swamp, if made according to this map, would reach far beyond the barrier and the explorable parts of the game world.

It also seems that the former mixture of forests and mountains (towards the demontower) was now a bit more differentiated to make it clear where the actual mountainous terrain south of the Psi Camp begins and where the marsh. 

The Abandoned Mine remained roughly at its place, but it is noteworthy that it was now south of the newly introduced northern river. The Old Mine remained at its place too, although the path was leading in a straighter line to the camp. The Free Mine didn't change its location either, but instead of a forest around it (and at some distance), it was now thightly surrounded by mountains, with a narrow path leading towards the mine. The same mountains that were leading all the way up towards the northern borders of the colony and all the way down towards the New Camp, only interrupted by the before mentioned pass.  

The "Old Castle" or "Old Fort" remained at its place (thereby disconnected from the New Camps fields) and was now drawn as being within or on the mountains, same as the demontower, which remained within the "cliffs in the southeast". 

In general, when compared to the Orpheus Map V1, apart from other additions and stylistic and atmospheric changes, it seems that this map was also an adjustment to the (expected) technical limitations regarding drawing distance. The mountains covering view between Old Camp and New Camp, the Free Mine being surrounded by mountains and the Psi Camp being covered from view by a big forest all seem to be added with these technical limitations in mind - at least as one of the reasons. 


## Ralfs Concepts

When Ralf Marczinczik joined the team he was given the task to create concept art of all the camps (these details will be dealt with in the world design docs), of all the other areas of the world and to develop Mikes visual ideas further, always in consultation with him. While he did not draw an actual map - as far as we know -, he has drawn concepts of almost every part of the surface. By connecting these images we get a good overview of the world as it would have been if created according to his concepts. 

And it *was* created at least partially - the world of v0.56 and v0.64b is corresponding to them to a large degree. But the world was incomplete and before half of the things were implemented, the concepts were already changed again, when new level designers took over and when Ralf as a concept artist was no longer involved. 
{: .subtext}

One of the things he changed was the conception of the marketplace (later exchange place). It was him or at least during his involvement in the world design, that the marketplace and the "cliff" (the latter of which now in a much, much smaller scale) became one again. In his concepts he was taking the idea of large, steep, even vertical mountains to the extreme, to serve as limitations to render less parts of the world simultaneously. According to his idea, the northern part of the world would have looked like this:

![Northern Part of the Colony in Ralfs Concepts](https://media.gothicarchive.org/conceptart/ralfmarczinczik/surface/Abschnitt_A1-A2-B1-B2.jpg)

We cannot go into detail here about how he conceived the exchange place to be - we will do so in the world design documents when dealing with the northern environment. But we can say that Mike did not approve this particular design and this was one of the things which - apparently - were not getting realised in the early models of the surface. While for most of the other areas they followed Ralfs evolution of Mikes former drafts, they did not do so in regard to the exchange place and the cliff. What Ralf kept more or less unchanged was Mikes idea of the northern forest. But the direct connection to the ocean where the player was supposed to fall into from the cliff did not exist in his concept. At least it does not look as if this lake or this direct connection to the sea is there (although the water from the waterfall seen on his concepts from the gamestart has to end somewhere but Ralf hasn't shown that) and if so it has to be very small. You can see how close the forest is to the mountains and there is no concept by Ralf showing this area, as far as we know. 

All of this leads us to the conclusion that Ralf deviated from this idea either consciously or due to a misunderstanding of Mikes map(s) that he was using as his source and inspiration. And it wouldn't be a surprise if he just didn't understand Mikes plan for the cliff and the marketplace immediately, as it does not become very clear on his maps (which is supported by the fact that Mike has drawn some sketches of how he imagined the cliff from the beginning unto Ralfs concept art - which was an usual practice for him in order to communicate what he wants to be changed).

The Old Camp did not change position and the Psi Camp did not change position either. On the concept below you can see the big forest hiding the view towards the Psi Camp that Mike had introduced on his sketch before. You can see the river he had introduced in the same sketch. And you can see the northern forest. 

![OC to PSI and Old Fort](https://media.gothicarchive.org/conceptart/ralfmarczinczik/surface/Abschnitt_A2-B2.jpg)

But there is one particular and important change that is to be seen here for the first time. In the south of the Old Camp you can recognise the mountains that Mike had added in his last sketch, potentially at least in parts as a natural cover between Old Camp and New Camp as well as towards the Old Mine in the south. On his sketch this terrain didn't serve any other purpose. But now the Old Fort was placed here, instead of unto or into the mountains further in the south, closer to the Old Mine, where the Fort was located on all of Mikes maps. It is also here during Ralfs involvement that the Fort was given its design (although it underwent several conceptual iterations). 

![OC to NC](https://media.gothicarchive.org/conceptart/ralfmarczinczik/surface/Abschnitt_A2_Tal-zum-NL-2.jpg)

Through all of Mikes maps the New Camp has always been in the south and the Free Camp in the north, now they switched places. The Free Camp was now in the south of the New Camp. And the New Camp had no longer any connection with the southern river, but with the northern river instead, that Mike had just added in his sketch before. And this is also how it was implemented in the first world models we know of or have access to, with the New Camp north of the Free Mine. 

Ralf has also given the bridge in the north of the OC its design, that leads over this northern river and can be seen here. And you can also see the hangman's tree south of the bridge. While it has been drawn in the west of the Camp by Mike, it was now placed north of it and this is also how it was modeled in the early versions of the game world, where this large tree was directly included into the world mesh (it was most likely modeled before Ralf created his concept for the tree, as it looks very different). 

The Abandoned Mine remained in the north, but not in the south of the river, now it was north of it and in the *west* of the exchange place. And please take into account, how drastically the reposition of the Free Mine changed the distance to the Abandoned Mine, which were supposed to be connected deep underground (a connection which also had played an important role in Alex Wittmann's story). 

![Old Mine](https://media.gothicarchive.org/conceptart/ralfmarczinczik/surface/Abschnitt_A4_Felsen-vor-AM-B.jpg)

The Old Mine remained in the south exactly as Mike envisioned it. Ralf just developed various details of the environment, added some mountains in front of it and so on. But the southern river that was once supposed to flow by here is not to be seen. Since the New Camp was now connected to the river in the north, - and such was the waterfall - they changed the origin of the southern river. It should now come from a waterfall in the very south (instead of the west), forming a lake underneath the demontower on his cliff in the southeast. To be more precise: One bigger lake and a smaller, hidden lake behind. From here the water would run in a river towards the Psi Camp just like before. 

![Southeastern Lake](https://media.gothicarchive.org/conceptart/ralfmarczinczik/surface/Abschnitt_B4_Turm-des-Dmb.jpg)

It is this lake that would later be totally disconnected from the demontower and in the middle of which the "sunken tower" would be placed.
{: .subtext}

Another area that was added during this phase in Ralfs concepts, was the [Hermit's valley](https://media.gothicarchive.org/conceptart/ralfmarczinczik/surface/Abschnitt_B4_Eremitental.jpg) in the south of the Psi Camp (and thus in the east of the demontower). He also made a [concept of the "pass"](https://media.gothicarchive.org/conceptart/ralfmarczinczik/surface/Abschnitt_A1_AlterPass.jpg) that Mike had added to his latest sketch in the west, south of the Free Mine (which at this point would mean south of the New Camp). The Troll Canyon was also modeled roughly at this time in v0.56c and v0.64b, but no concepts by Ralf are known from this area. 

Then there was the addition of the [fogtower](https://media.gothicarchive.org/conceptart/ralfmarczinczik/surface/Oberwelt_Nebelturm.jpg). We know that the fogtower was supposed to be located at the "border of the swamps", much closer to the Psi Camp, and not at the location that the players may know from the final game, the location where Mike had originally conceived the stone circle to be. The gong on top of the tower was supposed to lead the player through the fog and thus towards the camp. This corresponds to one of the early world models, where two fogtowers exist. One placed close to the swamps, where it was actually meant to be. And one at the position where Mike had drawn the stone circle. Due to the existence of two identical towers in this model, we have to assume that one of them was a placeholder for something else, such as another tower. This is not too far-fetched, based on the existence of another tower concept by Ralf, the [lighthouse](https://media.gothicarchive.org/conceptart/ralfmarczinczik/surface/Oberwelt_Leuchtturm.jpg). 

![Runetemple](https://media.gothicarchive.org/conceptart/ralfmarczinczik/surface/Oberwelt_Erweckungsplatz.jpg)

When the stone circle was supposed to be replaced by the lighthouse in this concept phase, what happened to the stone circle then? The stone circle was replaced by Ralfs idea of the "island of resurrection", for which he was inspired by the "Island of the Dead" by Arnold Böcklin. More on this idea in the world design docs. 

And this is basically it. The world was in the process of being made according to these concepts until at least v0.64b. Flatzer made a map of what was actually done in v0.64b:

![Reconstructed Map of Demo 5 by Flatzer](https://media.gothicarchive.org/research/worldmap/flatchergoth/SFRender.png)

* All the three camps were already modeled at this point, not that much about them would change anymore (and not that much of Ralfs concepts was actually realised in them).
* You see the New Camp now in the north (it is more in the middle of the map, but north in comparison to the south in which it was originally meant to be), you also see the northern river running towards it, but in the model it was not yet connected to the camp. 
* The Psi Camp already being a swamp, surrounded by forests (later these forests were supposed to be made bigger and without these gaps inbetween). You also can see the coast line as in Mikes sketch, but here it is completely disconnected from the camp, unaccessible mountain terrain. And for unknown reasons the river from the south did not flow into the swamp as drawn on all the maps, but directly into the ocean north of it.
* You can see the fogtower at the former position of the stone circle in Mikes maps. 
* But no trace of the monastery ruins, which are also not known from any concept arts or sketches. 
* You see the big northern forest and the "lake" directly connected to the ocean (but positioned a bit higher than the ocean).
* You see the first approaches of "the cliff", which is the structure north of the forest with this small "gulf"-like sea (which was actually not that small in this world model with almost the size of the Old Camp), where the player would swim towards the northern forest.
* The Troll "Canyon" or rather a pass with the troll inbetween is seen in the northwest of the Old Camp, in the west of the forest. According to Mike's maps it must either have been this path leading to the exchange place or this must have been the early version of the "pass" out of the valley. 
* In this case the path to the exchange place (as well as the exchange place itself) was not yet included in this model and would need to run upwards directly west of the forest (please note that this map is a reconstruction, not original and it is not 100% accurate; for instance, the scope of the barrier is not correct here; the northern border would be lower and it would not reach as far into the east either)
* It is also here, at the (not yet existing) crossroad, where the entrance to the Abandoned Mine would have been modeled according to Mikes map.
* The Free Mine was not yet modeled either, but it was supposed to be placed behind the small gap in the mountains that you see south of the New Camp. 
* East of this entrance to the Free Mine and directly south of the Old Camp you can see the tall mountain with the Old Fort, as it was placed here on Ralfs concept.  
* The very big gap in the mountains in the southwest was supposed to become the entrance to the Old Mine. As you see, in opposition to all the map sketches, in the actual modeling approaches it was far more in the west instead of directly in the south.
* And the two lakes here in the south of the map, these are the southern lake and the "hidden lake", the demontower was meant to be modeled here directly east of these lakes on a cliff. But at this point a tower model was not yet made; the terrain was totally flat. 
* Please note that the Mountain Fortress, the Orc Cemetery, anything like an "Orc Area" and so on did not only *not* exist in this world model, but there was also *no conception* of them; they were not supposed to be there. 



## v0.7 - v0.9

With ~v0.7, when new level designers joined the team, namely Horst Dworczak, Mario Röske and Sascha Henrichs, huge changes to the world were introduced. We will list them below, but will not go into too much detail and will not show corresponding screenshots, as that will be done in the World Design docs.

![Map07-09](/_img/story/map/OW2.png)

* The exchange place was modeled for the first time. It did now lead very steep upwards, like Mike had imagined it. But the cliff separated from the exchange place with a direct connection to the sea was removed and instead only the small lake below the exchange place remained. The [exchange place was now looking](https://media.gothicarchive.org/screenshots/orderedbylocation/surface/EP/088.png) very similar to what you know from the release version, just with the proper original ropeway and with a higher cliff. The northern forest was also removed in this process and the Abandoned Mine was added close to the exchange place (originally with its entrance on the other side of the road). 
* The Old Mine has changed its place for some reason and was moved from the south to the northwest, as known from the release version and a "new" old pass out of the colony was added close to the Old Mine.
* The Free Mine was added in the south of the New Camp as well as a connection between them, both of which had almost nothing in common with the concepts by Ralf. 
* The southern lake remained, but for some reason the Demontower was not placed on the supposed-to-be-modeled cliffs east of the lake and directly above it, but in quite a distance, west of the lake. While it can be argued that the tower was still positioned on a "cliff", it was not very high (it once was supposed to have this feeling of a tower high on the mountain). There was still a lake below it, although a smaller and different one, and there was one behind it too, which you could see as a new interpretation of the "hidden" lake from the concepts before. The Demontower was now roughly at the position where originally the "Old Fort" was meant to be according to Mikes concepts. 
* The Demontower looked more like the later "sunken tower" in ~0.7+ and was then in ~0.8 changed into the much bigger tower from stone known from the release version. The original demontower was then re-used as a sunken "magictower" in the lake behind the Old Fort instead.
* The original "Orc Area" was added between the demontower and the Stone Circle, with an entrance to the OrcCaves dungeon. 
* The Fogtower remained at the former stone circle position only; no tower was left close to the swamp where the fogtower was meant to be and the lighttower didn't seem to have been modeled either. 
* The Swamp was modeled, but with a very limited scope, since they didn't follow Mikes last sketch with a long coast in the middle of the east, but chose to let the Swamp transition into the sea almost immediately behind the Psi Camp. 
* The idea of the "Island of Resurrection" was discarded, instead the stone cirlce was modeled at its release position. 
* The "Old Temple" was added (this is referring to the original model of the later so-called Monastery Ruins) on the other side of the northern river, where it flows into the sea, opposite to the fogtower.
* The Goblin Cave was added at its release position, although it was seemlessly connected to the beach of the warans in the release version; the water didn't run down here.
* The Entrance to the Orc Cemetary was added.
* Quentin's Camp was added.
* The Troll Canyon from 0.64b was moved to a bit of a different position, higher up the mountains close to Quentin's Camp.
* The friends meeting place was added.
* The way leading up towards the Old Fort was changed significantly.
* A plateau was added with a hut (Gilberts hut at this point). It may be what Ralfs idea of the "Hermit's Valley" developed into. 
* A forest was added in the southwest between the Old Camp and the new Orc Area (referring just to the small terrain with the entrance to the orc caves, not to the later version of the world, in which "Orc Area" refers to a much bigger terrain).

It is this map that the players who waited for Gothic before its release were familiar with. It is this map of which the most alpha screenshots exist and which was promoted the most. It had a significant impact on the expectations of the players and their perception of the game world. 


## ~v0.94 - 1.00

There is still a lot that has changed from the map above towards the final map. But it all was done in the last few months of development, to the surprise of many players who expected many things to look like as they were shown before. The following things were added or changed, resulting in this final map: 

![MapFinal](/_img/story/map/OW4.png)

* The Psi Camps prominent and unique temple tree was removed and instead the temple from stone and its stonen front court were added known by players from the release version. 
* The Monastery Ruins were redesigned into the strange mess we know from the release version (noteworthily a tower appeared with some similarities with the fogtower that could be interpreted as an early model for the light house conceived by Ralf).
* The Path leading down the exchange place into the valley was moved to its position from the release version at the outside of the mountain instead of further north inbetween the mountains.
* The cleft from the Troll Canyon was removed, probably because the Troll didn't throw any gobbos anymore anyway as that feature was cut - and did not anymore live in his troll hoard, just wandering around in the "canyon"; perhaps also because of bad behaviour of the Gobbos falling into the cliff and/or pathfinding issues when it was decided that Diego should be there with the player. <!--even if it is hard to call it "canyon" with it being just big flat plane surrounded by mountains. -->
* A little recycled Orc village was added at the former OrcCave entrance due to the removal of the underground OrcCity which to implement was no time anymore.
* The whole area betweenn the Old Camp and Aidan was changed significantly, Cavalorn's hut was added as well as the path towards the totally unused Orc "arena" (which was not a concept of any design concepts and didn't have any purpose in the story either as far as we can say). 
* Due to the redesign above of the plains between OC and Aidan the forest in the southwest didn't fit here anymore, was removed and instead placed northeast of the Old Camp.
* The entire mountain fortress was added. The fortress was basically placed at a position where originally the Demontower was supposed to be on both Mikes and Ralfs concepts, while the Demontower itself was placed roughly at the position where Mike originally envisioned the "Old Fort". 
* The Old Pass was removed again with the path just suddenly ending in a mountain wall. 


## Sequel Concepts

In the original Gothic Sequel the layout of the world was obviously defined by the release version of Gothic and wasn't supposed to be changed. The world would still have been limited to the colony. Inspite of the destruction of the barrier that would allow them to display parts of the outside world, they did not plan to add additional terrain. Not because they didn't want to, but because they weren't able to in lack of time and level designers in the Sequel team.


<div class="authorship">
    <img src="/_img/authors/flosha-sm.png" alt="Flosha">
    <p>
        <strong>Author:</strong> Flosha<br>  
        <em>Creative Director</em><br>  
        <br>
        <strong>Created:</strong> 27.03.2024<br>  
        <strong>Last Change:</strong> 07.04.2024  
    </p>
</div>


## Read next

* World Design (wip)

