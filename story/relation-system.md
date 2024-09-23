# Relation System

```
Author: Flosha
Written: 29.09.2021
Last Update: 17.09.2024
```
{: .info }

*29.09.2021*

When confronted with the complexity of the story that we had reconstructed according to all of the early ideas and shaped according to our own, the questdesign became a struggle and we were in need of order in this chaos. It was too complex to keep an overview. We needed a system, a scheme.

Thus, I came up with a scheme of relations both as a system of ordering quests and keeping an overview of them, as well as a method or a tool of designing them. All the missions in the game, which, in a rpg basically mean: all the things the player is supposed to do in a given playthrough, had now a specific *function*. 

By this system we knew which kind of quest we would need to have at which point of the story just in order to fulfill a specific *function* without even knowing anything about the content of that quest.

That made the complexity as simple as it could be. It is something we may have been inspired to by Alex Brüggemanns approach to gamedesign: If you want a strong story with convincing motivations and so forth, you need to simplify. Thinking of functions instead of actual content made that easy and inspired the content by itself. 

We knew what is the purpose of a quest and at which point and between which camps, guilds or npcs will it take place. As a designer we could now look at the scheme and see which kind of missions were still needed to be done and fill in the details, by following a scheme.

But how does that work?


## Background

*17.09.2024*

My relation system idea is inspired by one particular approach in the old Phoenix Main Mission document. In order to join one of the camps, the developers suggested *four* missions that each contained a decision. 

The player should get one mission that resolves in a decision between either the New Camp or the Old Camp, one that resolves in a decision between Old Camp and Psi Camp. And one between Psi Camp and New Camp. 

But since the player could in theory solve these missions as such, that he decides them for a different camp every time, thereby getting a plus point for all of them, there should be one final quest by which the decision for a camp would be definitely decided. 

In this final mission all the three camps were involved; depending on his decision he would then be committed to one of the camps.

Please note, that at this point of development, the original idea of the four classes was already discarded. No longer was the player supposed to be able to complete the entire game as a Thief. Therefore, their scheme was quite a bit different than ours had to be. 

But based on this idea I came up with the system described below. What is written below is basically just taken 1:1 from my internal notes for the team at the time of writing, just in order to show how I developed it and explain the thought process behind it. The important part is to do the work that I have outlined there in form of the tables I suggested. 

The article has to be structured better; many things may be possible to condense much more, but I post it now as is, in order for some of our contributors to be able to work with the suggested ideas. 


## How I developed the system

*29.09.2021*

I started with how we could have a sort of logic of the player, how he would join the camps, which is the initial task in the first chapter. 

The quests as they have been written in the original document as described above, where limited in so far, as that they were written on the premise that they player is inside of the Old Camp and gets all the quests from there. But the player would also have been able to go to the New Camp immediately or to the Psi Camp very early on. In this case, there also should be missions given in these other camps as well (ofc these missions can also be the same ones but given from the other side) to serve as a decision tree between the camps and by which the player can develop his character into this direction (of preferring Camp X). 

Additionally, with the Free Camp we have one camp more that we had to consider. So we needed one additional OC vs. PSI and NC vs. PSI quest in the Psi Camp and with the New Camp and Free Camp accordingly. Thereby I ended up with the following structure:

```
OC:  OC ⇆ NC | OC ⇆ FC | OC ⇆ PC
FC:  FC ⇆ OC | FC ⇆ NC | FC ⇆ PC
NC:  NC ⇆ OC | NC ⇆ FC | NC ⇆ PC
PC:  PC ⇆ OC | PC ⇆ FC | PC ⇆ NC

FINAL: PSI ⇆ OC ⇆ NC ⇆ FC
```

I call this structure the "InterCamp Relations".  
This is the logic and the low level decision-tree (the basic level of the "Entscheidungsbaum") I mean, in the first chapter. First comes the decision between a camp. But I thought: We should proceed in that same manner. So after the decision between a camp, there comes the second level of the decision tree, looking like this:

```
OC:  STT ⇆ GRD ⇆ KDF
NC:  ORG ⇆ SLD ⇆ KDW
FC:  SFB ⇆ FLL 
PSI: NOV ⇆ TPL
```

Here it is about decisions between the guilds and the related classes. So its about content (not always has this to be done in form of missions, it also can just be dialogues etc. or environmental storytelling) that deals with the relationship of all the three guilds with each other so that the player can decide between them in some form or another. 

Important to note: This decision for a guild or class may already be included and interwoven with the before mentioned camp decision missions; because during the camp decision, you are already dealing with specific guilds of these camps and you may solve these missions in the interest of one of these and not the other, for instance. 
{: .subtext }

But then it goes further when you are involved with one of the guilds already, like in the early stages of joining. Then it is about the relation to a particular other guild in the camp.

For the Old Camp, the following "relations" have to be covered:
```
STT: STT ⇆ GRD | STT ⇆ KDF | STT ⇆ VLK | STT ⇆ EBR
GRD: GRD ⇆ STT | GRD ⇆ KDF | GRD ⇆ VLK | GRD ⇆ EBR
KDF: KDF ⇆ GRD | KDF ⇆ STT | KDF ⇆ VLK | KDF ⇆ EBR
```

But the relation of these guilds can be dealt with (not necessarily must be) by the same mission. For instance there is one mission that you get both as a KDF and as a GRD and depending on your guild and who you are working for, you experience a different side and perspective of that relationship between the two guilds and that mission. Therefore, the scheme for the OC can be simplified into, what I summarise as these "IntraCamp Relations":

```
STT ⇆ GRD | STT ⇆ KDF | STT ⇆ VLK 
STT ⇆ EBR | GRD ⇆ KDF | GRD ⇆ VLK 
GRD ⇆ EBR | KDF ⇆ VLK | KDF ⇆ EBR
```

In the same way, the player may solve specific missions in a specific *playstyle* that we associate with a class; thereby not ruling out a specific camp at first, but other classes. So just as the scheme above, there could as well be the following scheme.

```
FIGHTER ⇆ MAGE
MAGE ⇆ PSIONIC
PSIONIC ⇆ THIEF
THIEF ⇆ FIGHTER
FIGHTER ⇆ PSIONIC
MAGE ⇆ THIEF
```

If writing missions with the function of letting the player make a decision between these two "classes" by solving the mission in accordance with that class or in favour of the guilds representing this class, he can thereby choose a class by roleplaying. 

To follow along with the guild example, it means concretely: After you decided for the Old Camp *and* for the Shadows, you have these missions:

(1) A mission that deals with the relationship between Shadows and Mages in the first Chapter. (2) A mission that deals with the relationship between Shadows and Thugs in the first chapter. (3) A mission that deals with the relationship of Shadows and the Barons. And (4) a mission that deals with the relationship of Shadows and the Folk.  

But when looking at it from the class angle. It would mean concretely, that, for instance in case of the Thief Class (1) the player would be confronted with a mission, that he can solve either through the fighter or the thief playstyle. (2) Then with a mission that he can either solve through the thief or mage playstyle and so on; both of these missions do not have to be related with just one thief guild but can for instance, be related to two or three of these guilds or even with none, but just in a general way, before even being confronted with a specific thief guild. After this decision he is then confronted, similar to before, where it was about the "IntraCamp" decision, with a "IntraClass" decision.

The player has decided for a class, but has now to decide for a guild. Instead of the approach of before, where the player has decided first for a camp and then for a guild. Both of these can be combined, can be mixed or may replace one another; one player may rule out the IntraCamp decision, as he makes a clear IntraClass decision beforehand; another one may rule out an IntraClass decision, because he made a clear IntraCamp decision beforehand, if you understand what I mean.

So in this case, the decision tree would be like this:

```
FIGHTER: GRD ⇆ SLD ⇆ TPL
THIEF: STT ⇆ ORG ⇆ FLL
MAGE: KDW ⇆ KDF
PSIONIC: -
```

But going back to the guilds, in order to explain the system:  
So there should be such missions that give you points for joining a guild before they consider you as a potential member. When you get two or more points they consider you as a member; by giving you the trials - KDF/KDW - or by offering you to join - STT/GRD and so on.  

And because the missions decide between this or that guild, the missions need to be structured in a way that they show a *relation* between the respective guilds, how they relate to each other and how the player relates to them. 

The *Stt ⇆ Kdf* mission either needs to show a relationships between Mages and Shadows where you play for or help either STT or KDF, and/or it needs to be a mission where you decide between the usage of magic or thief skills or between mages and thieves virtues.

The same with KDF ⇆ GRD and GRD ⇆ STT.
This offers at the same time the perfect opportunity to show these different relationships - and nothing gives the world more depth than more pronounced/developed relations.

---

Concretely, in order to develop these missions the best, we need to create inter- and intra guild relationships. For this we look at the CH1 Guild Attitudes and what the guilds say about each other in Mikes Guild docs and the 0.56c info pool. Then we write short descriptions summarising the relations of each guild to each other, one camp at a time. 

---

And these relations are not just meant to be dealt with *once*, e.g. in the first chapter in order to decide between these guilds, but they should be dealt with throughout the story in each chapter, to serve the function of informing the player and involving the player in the *changes* of these relationships in course of the story.

An example for a mission of the STT ⇆ KDF relation, would be in CH3, when the Mages start to slowly oppose the barons, where the Shadows may try to get infos and spy a bit about what the Mages are doing/planning, as the distrust of the barons increases.

This can and should serve as the basic outline and principle of quest relations: Look at how the attitude/relation between guilds evolves in the course of the story, write dialogues and a mission reflecting that. 

This way we can get a really nice overview of the missions we need to do, while *everything* is deduced from the main plot and its correlation of the guild attitudes. Every mission can then be seen in the context of the story; everything is connected and nothing is out of place. And this gives rise to an actual system of quest writing.

Via inter-camp, inter-guild (which means intra camp) and even inter-character (which often means intra-guild) relations. 

Thus, at every new situation in the course of the story we ask the question: How did the relation between Camp X and Camp Y evolve? How to reflect upon, display, represent and/or show this in dialogues, missions and texts? 

In the same way: How did the relation between the guilds of a specific camp evolve? Then: How did the relation between characters inside guilds (potential conflicts inside guilds) evolve? And so on. You get the logic.

No, we have to do this from outside to inside.
Starting with the big stuff:

* Relation between Gods
* Relation between Gods and Men 
* Relaton between the Realms
* Relation between Colony and Outside World
* Relation between Humans, Orcs and Half-Orcs
* Relation between Camps
* Relation between Guilds
* Relation between Individuals

This will rule and guide our quest writing.

For instance: Conflict of outside world and colony: The king doesn't send enough stuff anymore because the prisoners didn't send enough ore! - Problem! So talk about it in the game, send a messenger to the exchange place to bring the king a message of what happened and why not enough ore can be delivered and so on. 

Conflict between humans and orcs: At the beginning there is not much, but it is mentioned, the orc war is going on in the background, there are the orc slaves in the mines. But this evolves: From the beginning, being totally in the background, to Chapter 5 with it being totally in the foreground.

Conflict between camps: E.g. the war between OC and NC.

Conflict between guilds: Like the VLK being fed up with the barons more and more over time. 

Conflict between individuals: How mages think about each other, how the barons try to get at the top, how shadows are jealous of each other and so on, and so on.

---

Just as with the story we can use what I wrote above as a scheme, to create a new table which follows based on it by showing exactly which kind of quests (in their *function*, not their content) we need to have in order to properly show all the things worth showing to tell the story in full and without missing all kinds of potential narrative aspects. Because every kind of mission is about how something relates to something else.  

And when having developed these tables and having an overview of how these relations are at gamestart and at a given moment in the story, then we can add the content.

But we at least have no trouble anymore thinking: Which kind of quest may we need, what may the purpose be, the basic assumption of it? Because this way, every mission will have a specific function *before* we even know what it may contain. 

And I want to make this in table form.

We need an inter-guild relation table, an intra-guild-relation table,
an inter-camp relation table and so on, each with a short description,
while the so-called "guild attitudes" give hints about the latter, but they are the AI side of it, while we will make a table showing the story side of it. 


So for example we create a table of the barons.

That shows the relation of  
Gomez to Arto  
Arto to Raven  
Raven to Gomez  
Gomez to Scar  
and so on.  

And how it changes from event to event.   
The same for all other npcs inside every guild.  
The same for all guilds inside each camp.  
For example, the brotherhood inter-guild relations will be the simplest (in CH1), because there will be no or not much of a conflict between the guilds. But there may come a intra-camp conflict where people are split independent from their guild (as some follow Kalom while other follow Angar and so on). Different for the New Camp. Where there are conflicts between Mercs and Orgas, between Free Camp and New Camp, between Mages and Mercs, between Mercs and Peasants and so on.

---

03.10.2021

Create a table that shows the development of the relations in the course of the chapters (or the main events: beginning, convoy, omfull, fmtaken, orcassault, nemesis), we need a table like that for the relations of:

* Colony ⇆ Outside World
* Inter-Camp [Oldcamp ⇆ Newcamp ⇆ Psicamp]
* IntraCamp/InterGuild [Kdf ⇆ Stt ⇆ Grd etc.]
* IntraGuild/InterNpcs [Gomez ⇆ Raven etc.]

Additionally, we need to create a big table, seperated in guilds, that gives a short description of every NPC with a name which: Includes a summary of etymological meanings of the name, what we make that mean in the story and how this NPC develops over the chapters; just his basic characteristics and quests involved etc.
This is what needs to be done now with the highest priority in the story-department.

On this basis we then create a mission table per camp + chapters which lists missions per function. Like: Showing the relation of X to Y and Y to Z.

Of course: Not every mission needs to have such a function of relation, we also can think of additional functions of quests, but those with relations as their main function are the most important quests that will be most relevant for the story logic and process, as they contain important decisions of the player.
And before we think about any specific quest now (unless someone has an inspiration), we will try to list the required quests per their function it is supposed to serve and apart from that we need to discuss what other functions a mission can or should serve.

---

In the descriptive tables, the InterGuild Relations are often identical to the IntraCamp Relations. In most cases, all the guilds of one specific camp have more or less the same opinion about all guilds from another camp and have no specific relation. For example, no digger, no guard, no spy has anything to do in specific with a Guru and nothing more with them as with templars or novices. And in general they think that they are addicted freaks and so forth, so that is something for the InterCamp Relation Matrix. 

Only in rare cases some guilds may have a specific meaning about another specific guild of another camp, for example the mages which are allies. But they keep being so till the end basically. What really changes a bit and what needs to be addressed throughout the game, are relations of the camps to each other and relations of guilds inside the same camp. 
It would be easier to keep the overview like that.
We would have something like this:

```
CH    GUILDS
----   KDF       STT       GRD      EBR     VLK
CH1 
CH2
CH3
```

But it may still be useful to have one big table where all the relations to each other are formulated in a short term like Mike did in his lists.

InterCamp Relations = IntraColony  
InterGuild Relations = IntraCamp  
InterNPC Relations = IntraGuild  

---

04.10.2021

In the tables Oliver created at first, we had a guild description combined with a description of guild relations separated in OC to NC, and NC to OC etc.; two-sided relations and all guilds together. That is way too complicated and not what I meant, as we discussed later.
And this complicated table only showed one chapter etc.

What we do instead is a table like this:

```
CH     OC<>NC   OC<>PSI   OC<>FC   ...
CH1
CH2
CH3
...
```

One cell in one table row describes the relation between the two together, not the attitude one camp has to the second and the second to the first. And from top to bottom you can read how it develops throughout the story.   
That is what I meant and its a big difference I think and makes things much simpler. The attitude from one to another is not what I meant with the relationship at one specific point, which is completely focused on the chapter and how the main events change the relationships.  
But concerning the description of the camps/guilds itself, we should make this in another table. According to the principle of doing one thing and do that well. 

So we have a table just describing the camp structure, hierarchy, feeling. We have one table just describing the guild structure, hierarchy, feeling etc.

And one table describing NPCs as said before. One table for each guild with the NPCs in that specific guild. Concerning the NPCs the table looks like this:

```
VLK         CH1   CH2   CH3   CH4   ...
Ryan        ...   ...
Marus       ...
Snaf
Jesse
```


Concerning guild relations, one table per camp: 

```
OC      VLK<>STT   VLK<>KDF   ...
CH1
CH2
CH3
CH4
```

What is written on the right side of the table and what is written at the top of the table depends on what will probably have more columns. The section that has more columns/rows will be on the left. There are definitely more npcs than 6 (as the chapters), and so the npcs are written on the left. In other cases that may be different, but not sure.

This structure is also simple enough that all the relation-tables can be in one document. The complete relations of the camps, for instance in all 6 chapters fit on only one page.

The complete intracamp relations (inter-guild per camp) fit on one page too. With four camps that means 4 pages. What will take more room are the npc relations per guild. That may require one or two pages per guild, with about 12 guilds.  
But we will stay under 20 pages with just descriptions of all relationships between instances of all sorts. I assume.  
And this will be our info pool from which missions can be easily deduced.  

---


### World Tables

I want that the descriptions follow some method. The tables describe relation(ships). While inside the world document what is important is to:

* describe the general atmosphere of a place
* name and shortly describe the most important locations in a place (for example inside the OC: Marketplace, Arena District, Chapel and so forth)
* link specific places to the guilds/people to be found there
* add a short summary of the most important basic facts about the history of the given location 
* add a short summary of how the location is supposed to change/evolve in the course of the story

We may seperate these descriptive sections into music zones.
If some area has a specific music zone of its own then that is a clear sign that we perceive it as a place that deserves to be looked at independently, because change in music indicates change in atmosphere and meaning.
Thus, I would seperately describe outside ring and castle, because they are supposed to be a bit of two worlds.  
So we need such very short descriptions of the following places, which in all cases should not exceed one page per section:
* Outside Ring
* Castle
* Abandoned Mine 
* Exchange Place
* New Camp
* Psi Camp
* Swamp
* Surface (general atmosphere and naming of most important places which have NOT a music zone of their own, like the forests, the citadell etc.)
* Mountain Fortress (should have extra music)
* Stonehenge (this too)
* Monastery Ruins (this too)
* Troll Canyon 
* Free Camp
* Old Mine
* Free Mine
* Demontower 

----


### NPC Tables

I would like you to begin creating the NPC docs just as I showed you above how to make the table of NPCs
concerning the npcs the table looks like this

```
VLK         CH1   CH2   CH3   CH4   ...
Ryan        ...   ...
Marus       ...
Snaf
Jesse
...
```

So one table per guild, listing all the npcs therein and then adding etymological descriptions shortly. Or actually, no.. the table above is for character development in the course of the story.
The etymological and general character/background description should be listed in a document on its own like this:

```
        Name/Etymology    Background/Crime/Profession
VLK
Ryan
Marus
Snaf
Jesse
...
```

You see? That is what we need for this.
We may add additional categories on the right, but the name and a short description of the background/crime etc. may suffice.

---

On the basis of this general character description we then create the table of character development. Remember to search in this channel for all the names we (or you) have clarified already.

> Conspired leaders of the Revolt, united by the torture they suffered, constituting a Mafia ruling the ore business, conceiving themselves as revolutionary successors of the orebarons, being conceived by others as either freedom fighters or oppressors.

This would be an example of how to try to condense as much aspects of them into the fewest words.  
And its one of the (or maybe the) most complex guild(s). Therefore I would say that no guild description should be longer than this.

---


### 27.04.2023

This I think is an extremely valuable tool for story writing because it cannot be underestimated how much guidance it gives. Just by having a big scheme of relations and having these relations between all kinds of factions, realms, entities, npcs, monsters, gods, camps, subfactions etc. as themes to deal with in dialogues or missions, we have a very clear plan of what to write about, what to deal with in dialogues. We don't have to get topics from nowhere, this big scheme is providing hundreds of possible topics to deal with and we can always take the scheme and see what we have to address.


## Relation Systems



07.-08.12.2023

Content (missions, items, environmental storytelling etc.) dealing with themes deduced from the relation system.

* Entity to Entity / Instance to Instance


## Relation Systems

Below I will list all kinds of categories of relations, or in short, "relation systems". By these relation systems we not only differentiate how one entity (or "instance") relates to another entity, - which I summarised as "Mutual Relations", - but also how one entity relates to specific *themes* of importance. These themes are partially defined by the story, but there are also essential themes we have to focus on based on the gothic-fantasy setting.  
This way the relation systems help us to have an overview and to address all the themes that one expects from the premises of our setting and our story, without falling into the trap of missing various essential themes and thereby wasting the potential of our own premises. 


### Mutual Relations

* Man to Man
* Group to Group
* Guild to Guild
* Faction to Faction
* Class to Class
* Camp to Camp
* Province to Province
* Realm to Realm
* Race to Race 
* Species to Species 
* Sphere to Sphere
* God to God

Examples: How Milten relates to Corristo (personal relationship), how the Shadows relate to the Orebarons (guild attitude), how Humans relate to Orcs (racism), how Innos relates to Beliar etc.
{: .info }


### Individual Relations

How an NPC, a guild, a species relates to all of the above. 

Examples: Relation of the Circle of Fire to the Orcs (Race). Relation of an Individual to the Clergy (Faction). Relation of a God to a Guild (e.g. how the Inquisition justifies their actions through Beliar). 
{: .info }


### Relation to Themes

*Flosha & Hagen, last update 22.09.2024*

We list the themes below in a rough structure. Many themes can and should be looked at from different perspectives. Thus, apart from the themes themselves, we also have to take these perspectives into account, from which we may have to deal with the themes. 

#### Perspectives

* intra-personal - how one relates to a theme based on personal history, emotionally, mentally or from a psychological point of view
* inter-personal - how one relates to a theme in relation to others
* political point of view
* ecomonical point of view
* religious/cultural
* historical (viewing themes from a historical perspective and different views on historical events)

#### Themes

* Freedom is the main goal of the game and thus also the main theme; at first it is a simple understanding: Be free by getting out of the prison that holds you captive. But Freedom has to be addressed from all kinds of angles: External freedom (breaking out of the prison) and internal freedom (free will?), freedom of choice, control or discipline as requirements for freedom, responsibility as a consequence of freedom; freedom in thought and feeling, freedom vs. imprisonment and all the different possible layers of imprisonment (in the colony, the city, in the realm, in society, in the war, in the body, in ones mind, in ones own conditioning and how to break free; freedom in relation to economic and political power, freedom by non-identification (with everything that can be enslaved), freedom in the sense of spiritual liberation and what it requires (action, belief, grace?), freedom of the gods, and how all of that correlates with, is presented alongside or in contrast to freedom and restriction in the gameplay and exploration. 

* Hierarchy & Bond: loyalty to X (king, kingdom, ...), rank, status, prestige, leadership & servitude, honour, sincerity, duty, responsibiliy, determination, blood & descent, family, clan, tribe, caste, class, guild, group, community - and can one be free in a hierarchical society? 

* Economical Themes: (Right) livelihood, labour, working conditions, exploitation, sharing, poverty/misery & wealth, greed, currency, property & stealing, the ore business, means of production, tools, food, hunger, harvest, lack & superfluity, free time and art, imprisonment by the constant struggle for survival. 

* War & Peace
* The Penal Colony
* The City
* Imprisonment & Freedom
* Crime & Criminals

Modes, Qualities & Conditions of Mutual Relationships: trust & betrayal, truthfulness & lies, affection, friendship & loneliness, love, partnership & desire, jealousy, dependence & independence, awe, admiration, disgust, disdain, respect, recognition, revenge, atonement & forgiveness


* Self-Image & Self-Reflection
* Competition & Sports
* Death & burial
* The dead & Ancestors 
* Magic & Rituals
* Rites and the Cult(s)
* Perception (and trust in their own perception)
* Age & Aging (Childhood, Youth, Maturity, Seniority)
* Blossom & Decay
* Hatred, Wrath/Anger
* Passion
* Temperance
* Happiness & Suffering
* Philosophical: (Free) will vs. Fate, Identity Formation, Violence vs. Non-Violence, Virtues & Vices, Role of the Gods, 
* Dreams
* Demons
* Health & Sickness: Disease, Wounds, Healing, Care, Medicin, Immunity, Vulnerability, Resistance, Possessiveness, the Plague, ...
* Ecological: psi-waves, psi-knots, magical rain, weather, vegetation, mutations, ...

<!--

## Faction-Relation Missions

07.12.2023

These missions or dialogues serve the purpose to show how the different factions relate to each other in CH7. In brackets the number of missions and/or the minimum number of dialogues so that at least the relation is adressed on both sides.

Refugee Camp <-> Inquisition (2)
Refugee Camp <-> Demoncult (2)
Refugee Camp <-> Tymorians (2)
Refugee Camp <-> Royals (2)
[Refugee Camp <-> Outlaws (2)?]


CH2
Inquisition <-> Priests (2)
Priests <-> Heretics (2)
Heretics <-> Inquisition (2)

Inquisition <-> Royals (2)
Royals <-> Priests (2) 
Priests <-> Outlaws (2)

-->


