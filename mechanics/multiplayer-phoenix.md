# Phoenix Multiplayer

``Author: Flosha``  
``Written: 03.11.2022``  
``Last update: 25.09.2024``  

Before reading this article you should read [/alpha-multiplayer](/mechanics/multiplayer-alpha).
The Phoenix multiplayer - if ever realised - will be divided into three sections, that can be chosen from the Multiplayer menu. There is the (1) *Story Mode* for up to 5 players + *"Bonus Stories"*, there is (2) the *Freeplay Mode* and there is what I call (3) *Scenarios* where each scenario is playable in one or more additional "modes". 

Please be aware that nothing of what is described here is currently worked at. It should be seen as an attest of a potential future realisation; of how a multiplayer story mode as imagined by the founders could be realised and of potential other modes that could fit Phoenix well; in many cases the technical framework has already been realised in the community, but the specifics are our unique concepts.  
{: .subtext }


**Content:**
* [Story Mode](#story-mode)
    * [Short Stories](#short-stories)
* [Freeplay Mode](#freeplay-mode)
* [Scenarios](#scenarios)
   * [*Arena*](#arena)
   * [*Survival*](#survival)
   * [*Raid*](#raid)
   * [*Assassination*](#assassination)
   * [*Convoy*](#convoy)
   * [*Ore Strike*](#ore-strike)
* [Unlocking Content](#unlocking-content)
* [Interface](#interface)


### Story Mode

For the story mode, as the "heart" of the multiplayer, we start by different premises. It must be as it is in any good story-coop where there are separate characters to be played. Never would or should a character say the same as another character or be told the same by NPCs as another character. The first solution, that Mike describes as very bad, we see as the only reasonable one, but only when seen in combination with pre-narrated characters. It is the only one that is in accordance with the design principles and the idea of a storydriven immersive sim rpg. 

Gothic/Phoenix offers such individual characters in form of the four friends, alongside the nameless hero they are the five playable multiplayer characters:

* `PC_HERO` (Hero)
* `PC_FIGHTER` (Gorn)
* `PC_MAGE` (Milten)
* `PC_PSIONIC` (Lester)
* `PC_THIEF` (Diego)

But the friends in the multiplayer shouldn't act as mere prototypes for additional heroes in the same shoes as the main hero; they should act in accordance with their role in the story.

The friends were convicted two years before the player, they already have a guild, a place in the prison hierarchy as well as an associated class, which solves all the problems regarding the first sixth of the game, by which Mike describes the first chapter.  
There is no need whatsoever to omit the first chapter, the only need is to think of the story from the individual perspective of the five characters.  

It is only consequent, that the other characters do *not* receive the same missions as the main hero (in most cases) and receive missions tailored specifically to them. And how could this be seen as a compromise? It is much rather a special feature.

In course of the story they can accompany the main player on his missions (like on the focus search or into the temple), but in the meanwhile there will be things to do that we have written for them specifically. Each of the friends will have dialogues and missions different from the dialogues and missions that are available to the other friends. 

In some cases the friends *may* be able to solve a mission, that otherwise the hero would. But in no case can the very *same* mission be taken by several players (they may just - at most - get an equivalent or a similar mission from the same or a different mission giver in a different context), nor can any player take a mission away from another, as it is never the very same. 

We call these the "character plots" and they will correspond to the events the player knows from the main plot and will fill gaps like: What did Diego do in the meanwhile? Why was he here? In some cases the Singleplayer will leave the player with some unanswered questions which are to be answered in the multiplayer by playing with the four friends. 

**Character Selection:**  
Before a multiplayer session, there of course has to be a character selection, where one of the players chooses the main hero, while others choose one of the four friends. If only two or three players play together just one or two of the four friends turn into player characters, while the remaining friends remain NPCs like in a singleplayer session. 

The game starts regularly with the conviction of the main hero. The story, missions, dialogues and available answers for the main player are the same as in the singleplayer mode. 

**Singleplayer to Multiplayer:**  
The idea of enabling a friend to join a singleplayer session in the middle of a playthrough is easy from a gamedesign perspective (the technical implementation is a different question) insofar as that every one of the four friends has a clear scripted state and position in the game world etc. at any given moment of the story and can then easily be taken over at a specific point in time by another player joining the game. This way, a singleplayer session should be possible to turn into a multiplayer session and vice versa. 

**Fixed Roles:**  
Exactly because of the story and in order to not compromise it, the other player characters are for sure *not* possible and not meant to be shaped as much as the main hero, because they already have a fixed role. In the same way, as the main hero interacts with the four friends in the story, where they give specific answers, the possible dialogue options of the players controlling the friends have of course to be restricted. This is *not* a compromise, it is the opposite, it means *not* to compromise the story for the multiplayer, but to tell it consequently while allowing additional players to participate. 

Examples: A session starts. One player chooses the main hero, a second player chooses Diego. The main hero is being brought to his conviction at the cliff, while the player in control of Diego spawns on the way to the Cliff. Both characters have their individual mission logs. While the main hero is convicted and it will be his first task to orient himself in the colony (the first chapter being the "orientation phase"), Diego has a mission and motives of his own: Going to the Cliff, checking out what's going on at the Exchange Place etc. 

The mission log books give us an opportunity for additional individualisation and differentation between the characters that will help to shape their identity. For instance, as explained in ``/mission-log`` the main hero writes in a book he is actually carrying with himself in a diegetic way, even though in past tense, thereby suggesting that instead of "writing" into the diary, the player, while playing the story, "unlocks" the entries that are slowly completing the story written down by him in a book after the events. This can not be the case for Gorn, for instance, who is illiterate. So whatever is written in his mission log, will be written by a narrator (who may not be able to retell the events accurately, so it may contain some speculation), not by himself. In case of every character we can think about how he may write and use a different background texture representing him. Lester, for instance, may write in a more chaotic way and not in a book, but loose slips of parchment pieces. 
{: .subtext }

While the main hero is baptised by the thugs, Diego *can* (not must) intervene. If he chooses to do so a dialogue with the main hero will be initiated, where the player character has the same dialogue options and Diego will say the same, in a fixed manner, as in the singleplayer too. The player may then choose to accompany Diego as in 0.94k or to proceed on his own. In any way, the player will have to go through the story as known, will have to join a guild and so forth, while the four friends will have to play their own story. 

**Parallel Stories:**  
Just as with every other character in the game, we have to assume that the friends are *doing* some stuff on their own while the player character is doing his. Of course in the release version this is not the case, because the world is almost completely static, nothing really happens behind the back of the player. But the story still at least implies that they do something and the original story even more so. In this way, the main hero and the four friends are confronted with each other and crossing their paths several times in course of the story. Things happen simultaneously and just as the main hero fulfills his role and takes part in driving the story forward or influencing it in some way or another, the friends too play an important role in the events, parallel to him.

The old story implies that the four friends are meeting several times in course of the story. In the Alpha, Gorn and Lester are at the meeting place already at the beginning of the game and after escorting the player into the valley, Diego tells the player, close to the bridge, that he now should proceed on his own, since he still has to do something. Later in the game, in course of the mission for Thorus of getting the list from the mine (it is not given by Diego), Diego seems to follow him and meets him in front of the mine. By the following dialogue and other, similar hints in the documents it is suggested that the four friends were meant to keep an eye on the main hero from the very beginning, they are working in the background, observing the player, talking about the events taking place in the colony and eventually helping him; while the main hero would slowly form a bond with the friends - and with one of the friends more so, depending on his choosen guild and/or class, due to which he would have the most to do with him.

For example: In this particular case, the player is send to the mine for a mission to become a shadow (not given by Diego as it was done in the release version, where the same man who has stolen ore from the ore barons a few weeks ago is now suddenly the "leader" of the shadows; this is of course not the case). But in any way, Diego is a shadow himself and in the singleplayer campaign of the alpha story it is suggested that he follows him. For the multiplayer story for Diego we can derive a mission from here; such as an obvious solution like this: The leaders of the shadows is sending Diego to observe the player during the mission, which makes sense. It is logical that a guild, which works similar to the Stasi of the German Democratic Republic, while training a new snitch, will have other snitches observing him at work in order to evaluate his loyalty and trustworthiness.  

So while being involved with the player, sometimes directly, sometimes indirectly, at the same time they would mind their own business: Lester is involved in illegal drug trade, Gorn is a Mercenary, but has friends in the Organisation and is involved in their raids that are completely despised by Lee. Milten is doing stuff behind the back of his master Corristo and keeps meeting with his friends he is not allowed to see anymore.

They all have their story and thus telling these stories is the obvious solution for the multiplayer story mode. While being linked to and taking place simultaneously to the events of the singleplayer plot, being part of that very plot, they each show the story from a different angle, tell additional tales in the world, develop the story further, give it more depth and complexity and provide answers to questions, such as: Why is Diego here, what brought him there, what did he do in the meanwhile, how does he relate to the other shadows? And so on and so on.

And since every character is experiencing his own story or the same story from his perspective with individual missions, these character plots could work just as well as additional singleplayer campaigns that can be played alone, in case of which the Main Hero would turn into an NPC; which guild he joins could be random, thereby adding an element of surprise to every playthrough. 

**Multiplayer Storytelling:**  
Regarding dialogues, in the multiplayer mode every single dialogue would have to have an additional condition as simple as:

```
if Player is PC_PSIONIC, then TRUE
```

Thus, depending on the character played, the NPCs would either talk to you or not and if talking to you they would only have dialogues specifically written with your particular character in mind. 

It of course should also be possible at any given moment for player characters to speak with each other; the friends are usually saying the dialogues that are known from the singleplayer, but there may be some additional options in order to communicate some general important stuff: Exchange items with each other, agree upon meeting at a specific location at a given time etc. 

But the reader may realise a difficulty of this approach to a multiplayer story: When e.g. the role of Diego is taken by another player, how can one make sure that the main hero and Diego meet at the desired time? For example: When the player is send to the troll canyon and Diego is already there. How can this work, since the player in the role of Diego may be finished already before the main hero arrives? 

**Coop Missions:**  
The answer is: In these particular cases, where two or more characters are supposed to be involved in a mission - which is the case in both the singleplayer and the multiplayer mode, the scenario has to be designed in such a way that the other characters are *needed* to solve the mission. There were missions supposed to be designed as such that one player alone cannot solve them. So a character cannot be finished here before another one is present and cooperates with him. 

> Alex Brüggemann: You control only one character, but NPCs may join for particular Quests. They can be helpful in solving Quests that are especially designed for multiplayer. (15.06.1998)

> Mike Hoge: In GOTHIC people can play both against and with each other. Playing together will pay, for there will be some extra puzzles that require at least 2 players. (15.06.1998)

And as far as time is concerned: It is totally true that in a "player-driven" game as I called it, it would be very difficult to make sure that the story progression of two characters is in synchronicity *enough* to enable them to experience events together. But in case of an actually "[story-driven](/lore/driven-by-story)" game as I described it, it is not much of a problem. As the progress here does not depend from the players but just from the point in time within the act. Since the story is taking place on a day by day basis and most events will occur not earlier or later just because of the actions of the player character(s), the time at which an event occurs or the moment at which two or more characters are meant to meet to play together or to help each other, is clearly defined in a particular time frame, which in practice results in something like "Day 5 at Dusk". Other than that: We are speaking of a local multiplayer, meant to be played by friends who want to experience the story together, as friends within the game. So being together at the desired time is obviously not a serious problem, as they will *want* to be together for these missions in question, while also being driven to be by the narrative. 


#### Summary

So, to repeat: Just as there are missions that are written only for the main hero, there are missions only written for one of the four friends. And while this may be a "shitty solution", to use Mikes words, due to the immense effort it takes, it is the most consequent solution. And the different multiplayer characters add a lot of replay value. Every character plot tells the story of what they have done parallel to the player, how they were involved with NPCs in the world; they reveal and deal with many aspects which in the singleplayer main plot are only hinted at, that the player only hears about or even doesn't know anything about. 

The developers had spend years with the development of the singleplayer story. In the end just a little fracture of the story they had developed could be implemented in the game as they had planned to. At the same time they have always said that the setting and this game world that they had developed for such a long time and with so much passion and love for detail, is so rich and inspiring and that they had so many ideas left that they could have made several more games within this world. 

But instead of doing so and following such a passionate approach, instead of telling these stories (the only project going into such a direction (the Sequel) was cancelled and its developers fired), they have thrown all of these ideas out of the window and began to do something totally different in form of the official successors, into which not even half of that passion went into (as they would confirm themselves), nor can they even be described as gothic-fantasy. 

While from a historical perspective it was necessary to do all the cuts in the end as this was the only way that the game could be published that otherwise would have been cancelled the same way as its Sequel, - struggeling a lot already with the realisation of the singleplayer story alone - the stories of the four friends would have been ideal material for addons of the main game. 

Of course they wouldn't have been able to write these four additional side plots alongside the main plot in time, to release them alongside the main game, but there is no need to do so. In an ideal scenario the multiplayer could have been developed one plot at a time, thereby expanding the Singleplayer story at first into a Multiplayer Story Coop for two players, then three, then four and finally all five, while at the same time giving the opportunity to patch the main game into a more complete state. 

And it also offers incredible incentives for the modding community. Because other than just telling new stories in different times and/or worlds, modders can make it their mission to create additional multiplayer characters for the game, thereby expanding the complexity of the story further and further. What if you could play the story in the role of Xardas? What if you could play the story in the role of Scar? You see what this amounts to. 

And if the technical side of this endeavour is solved, - and there is some work being done in that direction by programmers involved in Phoenix, among others - this is definitely the direction we would choose. Time will tell if this dream comes true. But it is clear, that the original Vision of Gothic will not be completely fulfilled without realising the Multiplayer Story Mode. 


#### Short Stories

In addition to the main plot it would be possible to tell specific short story episodes which aren't taking more than 1-2 hours, such as replaying specific events of the past. These bonus levels or "short stories" function like little mods on their own; the gameplay mechanics are the same as in the main game without any specific multiplayer simplifications as they'll be described below in case of other multiplayer modes. 

Examplatory Short Stories could be:  
* **The Revolt (Rise of the Barons)**: An extra level where the prison and the castle is shown as before the revolt, the tower is intact etc. and you can play the revolt with one or two of the barons or other convicts in coop, initiating the revolt, killing the guards, including some dialogues etc. 
* **Bloodnight**: You play as the friends during the Bloodnight, fighting against the insane that led to Gorns trauma meant to be dealt with in the Sequel until the escape from the colony. 


### Freeplay Mode

Potential freeplay mode as known from STALKER utilising the entire game world, that could in theory be opened up to a significant number of players who would then be able to play their own stories here without a pre-narrated story, with a simulated A-life, including occasional respawns of monsters, items, trading inventory updates and so forth. 

Freeplay could potentially be combined with a hardcore Permadeath (the possibility of resurrection, as planned in the Alpha, which then would require help of other players, could make this more endurable). This could also be combined with the idea of switching into the role of any other random character in the gameworld, when the former one dies, so that every NPC can potentially turn into a player character. Many other interesting ideas can be realised in such a mode. 


### Scenarios

Apart from the entire gameworld, as being used in the Story and in Freeplay, there are also separated multiplayer levels, which we call *Scenarios*.

In form of these Scenarios, similar to the Short stories, we can use multiplayer maps to expand the storytelling. 

The Scenarios can be selected in a level selection menu. Each level appears under its specific name and either a screen or a short video (as in the 0.64 main menu), with tags below that tell which multiplayer mode(s) the level can be played in.  

There are six multiplayer modes (apart from Freeplay and Story):

* *Arena*
* *Survival*
* *Raid*
* *Assassination*
* *Convoy*
* *OreStrike*


#### Arena 

Battles in various smaller or larger, literal or metaphorical "arenas" from the game. May be played in form of Deathmatch (1vs1), Team Deathmach (e.g. 2vs2) for larger arenas, in Coop against hostile NPCs or even in Singleplayer against NPCs, in which case the Arenas can serve as well as practice of the combat/magic system in general.  

Most arena levels can be played in both Arena and Survival mode. The levels are unlocked by playing the Singleplayer. 

A timer is running and players respawn with a short delay; the fight is going on until the time is over, who has more points wins. 

Ideas: Instead of points given for killing enemies only (or at all), we could make it more tactical and stylish and create a better flow by giving points only for (1) silent kills, (2) parades, (3) evasions, (4) healing of friends, ...? This will be possible to think through better when the combat system has been done, which will make Deathmatch in Phoenix more interesting than it would be in Gothic now.  

Arena as well as survival may be possible to be played by various multiplayer characters that have to be unlocked in story mode (just as the arenas themselves). 


#### Survival

> "The goal is to survive and to escape".

Fight against waves of enemies, either alone or as a team of friends against AI. The number of players (up to 5), which enemies will spawn and how many in how many waves will depend on the level and is pre-scripted. 

An "Endless Survival" mode can be selected with the potential of player rankings by the maximum time they manage to survive.  

A similar thing has been done already for Vanilla Gothic in form of the "Left 4 Gothic" mod. 
{: .subtext }

Examplatory Survival Scenarios:  
* **Old Arena**: A fight against all kinds of human warriors becoming progressively stronger. 
 * **Orgy Madness**: The orgy going wrong; a big fight inside the Swamp where everyone is suddenly going mad; dead novices wake up again, possessed by the Sleeper. 
 * **In Flames**: Secret <!-- The Firemages fight against waves of guards and shadows coming; when all the mages are dead, another level is loaded as a bonus, where you play Corristo in the prison. The player who survived the longest gets to play Corristo, the others watch. He is alone but with mightier spells, more room to move and some possibilities to interact with the environment. -->
 * **Orc Assault**: Survive against the Orcs in the Outside Ring.
 * **Death to the Barons**: A fight in the castle, where the player can be one of the five barons and they try to survive against the waves of shadows and diggers storming the castle. 
 * **Orc Arena**: A fight against all kinds of monsters and orcs with progressive difficulty.
 * **Bloodnight**: Survive against the Madmen at the Pass. 
 * **The Great Hall**: A fight against waves of undead in the great temple hall.
 * **Demon Invasion**: You are in the demon world and have to survive against all kinds of demons, illusions etc., spawning all around you. 

Since these levels are more about the fighting, we keep it fair and fun and simplify things; instead of the need to grab an item with an animation, items will spawn as fat floating items you just have to run through as in Retro Mode. In some levels, like the *Old Arena* or *In Flames*, those items will spawn at specific points in the map like in Unreal Tournament. In other levels, like in *Orgy Madness*, the *Great Hall* and *Demon Invasion*, the enemies will drop stuff. This way the player can regenerate health during the waves and sometimes mid battle. Health immediately heals you, mana fills up immediately etc.


#### Raid

This mode is a mixture of survival and Team Deathmatch. In difference to Survival it doesn't only go against AI (which remains an option in lack of players); so there are two teams, both playable and both teams respawn. The difference to Team Deathmatch is, that there is an overarching goal like "take (or defend) the mine", that there are rounds, that you can only respawn in the next round and that the spawn points change with every round. A round is over as soon as all members of one team of a given round are killed or when a specific time has passed. 

The attacking team is called "Raiders", the defending team is called "Defenders", but that can change depending on the level and the corresponding lore or background of those teams.

Examplatory Scenario:
* **Free Minr Raid:** A fight around and within the mine leading you deeper and deeper. The more the raiders can push the miners down, the faster the respawn points are set deeper. The defenders lose when the Free Mine is "taken" and the raiders reach the natural caves, where the last survivors can escape into (if we should also include a kind of campaign, where two teams need to fight through different raids one after another, these escapes should give bonus points inspite of loosing). The defenders win when they can hold the enemies back long enough until some help from the New Camp arrives. 


#### Assassination

One team has all the available shadow tactics and tools, the others are bodyguards. The target is an NPC that goes specific routes and the bodyguards can only influence the route slightly. They can talk to the NPC and convince him to go another route, which will lead to different scenarios each round. The target is the boss of the bodyguards, which gives instructions to his guards, he will send some of them away to guard at another spot and will become angry if they keep surrounding him all alone. Here think of the Multiplayer of Splinter Cell 2, which should inspire us. 


#### Convoy

One team needs to get a convoy from A to B, the other team has to attack them. The interesting part is that the attacker team can chose a few different spawn points to attack from somewhere else and the convoy team, while starting as always, can decide to take a different route; this leads to surprises and different tactics. The game is over when
* the convoy reaches the destination (trigger zone) or
* the attackers have acquired the delivery before that

The delivery can be a cart drawn by an Orc Slave, a message by someone who is escorted or a backpack. There can be NPCs involved who move the cart and the convoy guards can give instructions or players may carry the delivery, wearing the backpack etc. This way they can also try to run away from attackers; which most likely will happen at a point, to evade the attackers and reach the mine, so its also a kind of escape-game. But who carries the backpack will be slower and cannot sprint as fast, so he always has to be protected or needs to hide. 

Exemplatory Scenarios (in the Colony) are:
* OC to EP
* OC to OM
* FC to NC
* PSI to OC


#### Ore Strike

Alongside Act II we may add an additional bombing mode, where an orebomb has to be placed at one of two or three spots like in Counter Strike. 

An examplatory scenario could be the whole castle with a closed gate plus prison. One bomb could be placed in the tower, one in the prison somewhere and one in the chapel or so. As in Assassination, players can use their thief skills (hide in shadows and other abilities) to make it hard to get catched. 
  
---

### Unlocking Content

Characters and levels are unlocked by progression in the Singleplayer or the Story Coop.

Examplatory Level Unlocking Conditions:  
* The OC Arena available right from the start (Deathmatch and Survival). 
* The Castle will be available after completing CH1 as Stt, Grd or KdF (Deathmatch).
* The Temple Tree will be available after completing CH1 as a Psionic (Deathmatch).
* The Orgy Madness after completion of CH2. 
* The OC Prison will be available in CH3 (Deathmatch and Survival).
* "In Flames" when completing CH4 as a Mage. (Survival)
* "FM Raid" when completing CH4 (Raid).
* The Orc Arena when completing CH5 (Deathmatch and Survival).
* The Temple LV2 Main Hall after completing CH5 (Deathmatch and Survival).
* "Death to the Barons" when completing CH5. 
* The Sleepers Block after completing CH6 (Deathmatch or "All against Sleeper"). 
* The MST Headquarter after completing the Singleplayer as Mst.
* The Revolt (Rise of the Barons) when completing the Singleplayer as Ebr.
* The Bloodnight in the New Camp when completing the Story Coop with Gorn.
* Demon Invasion when completing the game on Nightmare Difficulty.

Some characters may be unlocked when you made a quest for them in the singleplayer.

Examplatory Character Unlocking Conditions:  
* Namib becomes available when you joined the Psionics.
* Raven becomes available when completing the feverdream mode as a OC loyalist
* Lee when doing so as a NC loyalist
* Angar when doing so as Psi
* YBerion will only become available when you complete the whole game in the Nightmare mode
* Xardas will be unlocked when completing the whole game in the Madness mode

This way we can reward the player and can give some additional incentives to play the game on higher difficulties. In the multiplayer mode they may be hidden or only hinted at by shadows, while one may see something like: "Unlock this character by ..."


### Interface

The multiplayer is selected via the main menu as known from the gameplay trailer from 2000. In the Multiplayer Menu, one may have the following choices:

```
* Story Mode
  * Main Story
  * Bonus Stories
* Freeplay Mode
* Scenarios
```

If he chooses Story Mode, he will go into an extra Story Mode lobby. For the story coop we assume that the player wants to do this with a friend and they can find each other there by sharing their data instead of being in a lobby with douzens of available coop sessions.

If he chooses Deathmatch or Scenario he will receive a prompt like:

```
"What do you want?"
* Host a Session
* Join a Session
```

If he chooses "Host a Session", he will be led to the level/scenario selection menu. 

A list of all levels will appear in form of images or short videos of the levels, that can be switched through horizontally with ``Arrow Left/Right``. Those who aren't unlocked yet *are* selectable but are displayed in a different colour, perhaps greyed out. Upon selection of a locked scenario, a text appears on a new menu-subpage that tells the player what he has to achieve in order to unlock it. Alternatively it may immediately be displayed on top of it.  
Under the image there is a short descriptive text of the scenario and tags of the availablr modes it is playable in. Here he has only two choices: Go Back or "Host Level". 

If he selects "Join a Session" he will be in a lobby that is a simple list of all available sessions in a frame. 

At the top he can toggle different modes on or off; so that he only sees survival, only assassinations etc. They are displayed by their respective scenario/level name, a tag behind them showing the mode and in brackets how full the server is and how many can join + the name of the host (when he hosts a session, he has to give himself a name) that will appear here, for instance:

* Old Arena (1/2) [flosha] #Deathmatch 
* Orc Arena (1/2) [logx] #Survival 
* Prison Castle (5/10) [Arbax] #Deathmatch 
* In Flames (3/5) [Auronen] #Survival 
* Free Mine (10/20) [Avallach] #Raid


#### Lobby

Upon selection of a running session the player lands in the multiplayer lobby, where other players join and the character selection happens. 

Ideally the characters would be switched through by Arrow-Left and Right and rendered in 3D with an idle animation; alternatively, pre-rendered images may be used. Just as with the levels, every character can be selected, but locked characters will be named "Locked Character" with a text underneath that tells the player what he has to achieve in order to unlock it (or it may not, in order for players to find it out for themselves).  

Ideally, the focus would be put on the character selection and on showing the characters specific stats (attributes, skills and equipment), while there would be a little chat window and an info box where the player can see if others are joining; the character selection has to happen by first switching to a character and pressing Enter. If a character is selected, this same character cannot be selected by other players anymore. 

It also would be cool if one would be able to play with exactly his character as he is equipped at that specific point in the singleplayer campaign; but only one `PC_HERO` should be allowed to be played in each session.


<style>
    main {
        background: url("/_img/bg/code.jpg");
        background-position: top right;
        background-size: 70%;
        background-repeat: no-repeat;
        width: 100%;
    }
</style>
