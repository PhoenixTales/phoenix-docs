# Multiplayer

``Author: Flosha``  
``25.09.2024``

Please be aware that nothing of what will be described here below is currently worked at. It is primarily an attest of a potential future realisation; of how the multiplayer story mode could be realised and of potential other mutliplayer modes that could fit into the game - much of which - or at least the technical framework of which - have already been realised in the community.  


## Story Mode

From the very beginning of the development, Gothic had always been promoted as having a multiplayer story mode (which we call "Coop" today). It was an essential part of the project that they wanted to realise, mentioned in always every single interview and several times did let it seem that they are actually proud of the concept behind their multiplayer, which was meant to be different than what players knew at the time. 

``Add quotes``

It was meant to be playable by 5 to 8 players (the announced numbers always varied in course of time) and only in local networks via LAN (online was too slow at the time).  

``Add quotes``

But then, somewhen in 1999, after 3+ years already had been spend to realise it, it was announced that the multiplayer has been cancelled by the developer. 

We will at first deal with the reasons for the cancellation which were explained in detail by Mike, before offering a critique of that reasoning from our perspective and in the context of our design philosophy. 


### Reasons for the Cancellation

``gothic.gomp.ch, 1999``
<!-- > **Simon Moon:** Was war der Grund, daß der Multiplayermode abgesetzt wurde?-->
> **Simon Moon:** *What was the reason for the cancellation of the multiplayer?*

<!--
> **Mike Hoge:** Schwere Probleme mit der Story und dem Game-Design.
Als wir damals mit Gothic angefangen haben, war es meine Idee, einen Multiplayer-Modus mit Story einzubauen.  
Wir haben seitdem viele Tage und Wochen mit der Lösung von Multiplayer-Problemen verbracht, weil wir das Feature um jedem Preis einbauen wollten.  
Relativ früh wurde uns klar, wie viele Probleme da dran hängen, vor allem was die Missionen (die bei der Entwicklung erst als letztes kommen) betrifft. -->
> **Mike Hoge:** *Heavy problems with the story and the gamedesign.*  
> *When we started with Gothic back then, it was my idea to implememt a multiplayer mode with story. Since then we have spend many days and weeks with the solution of multiplayer problems, because we wanted to implement the feature at all costs.*  
> *Relatively early it became clear to us, how many problems are involved in that, especially concerning the missions (which come last in the development process).*  

<!-- Einige Beispiele:  
Problem: Die Missionen von Gothic bauen teilweise aufeinander auf. Es gibt Packs von 5 oder 6 Missionen, die teilweise aufeinander folgen müssen aber auch teilweise parallel verlaufen können. Spieler A nimmt Mission 1a an. Mission 1b kann erst losgehen, sobald Mission 1a gelöst wurde. Spieler B spricht mit dem Auftraggeber, kurz nachdem Spieler A Mission 1a gelöst hat und bekommt Mission 1b OHNE Mission 1a gemacht zu haben oder überhaupt zu kennen. Das ist Mist. -->
> *Some examples:*  
> *Problem: The missions of Gothic, in some cases, build on each other. There are packs of 5 or 6 missions, which partially must follow each other, but can also partially run parallel. Player A accepts Mission 1a. Mission 1b can only start when Mission 1a was solved. Player B speaks with the mission giver, shortly after player A has solved mission 1a and gets mission 1b **without** having done or even to know mission 1a. That is crap.*  
<!-- Mögliche Lösungen:
1. Spieler B bekommt die Mission nicht - alle Missionen dieses Strangs müssen von Spieler A gemacht werden -> Scheißlösung, denn wir müssten uns bei 5 Spielern 5 mal so viele Missionen einfallen lassen.
2. Einer der Spieler bekommt immer alle Missionen, und die anderen müssen ihm "unfrei" als Party folgen -> Problem: Jeder möchte gerne Missionen annehmen können.
UND: So würden immer alle Spieler überall gemeinsam hinlaufen. (Das wiederum ist ein weiteres Problem)-->
> *Possible solutions:*  
> *1. Player B doesn't get the mission - all the missions of this string must be done by player A -> shitty solution, because in case of 5 players we would need to come up with 5 times as many missions.*
> *2. One of the players always gets all the missions and the others need to follow him "unfree" as a party -> Problem: Everyone wants to be able to accept missions.*  
> *AND: This way, all the players would then run everywhere together (which in turn is another problem).*  

<!-- Weiteres Problem: Rennen immer alle Spieler in denselben Dungeon (was teilweise aufgrund der voranschreitenden Story nicht zu vermeiden ist, denn wenn das z.B. große Portal zum uralten Tempel aufgeht und alle NSCs rennen hin und plündern, dann wollen die Spieler natürlich alle mit von der Partie sein), dann können viele kleine feine Sachen in der Story so nicht stattfinden, weil die Herausforderung für einen Spieler einfach in einem magisch- psionischen- pfeilgespickten und blutsprizenden Inferno von 5 Spielern zunichte gemacht wird.
Wir wollen kein Diablo machen. --> 
> *Additional problem: When all the players always run into the same dungeon (which is partially unavoidable due to the proceeding story, because when the portal to the ancient temple opens and all the NPCs run there and plunder, the players of course want to take part in it), then many small, nice things in the story can't happen like that, because the challenge for one player will just vanish in a magic, psionic, arrow-studded and blood-splattering Inferno of 5 players. We don't want to make Diablo.*  

<!-- Noch ein Problem: Im ersten Sechstel des Spiels ist der Spieler in keiner Gilde. Er entscheidet sich, wem er beitreten will und macht Aufnahmeprüfungen. Diese können auch nur einmal gemacht werden. Also schonmal dasselbe Problem wie oben, 5 mal so viele Missionen.
Darüber hinaus gibt es hier aber noch das Problem, dass das Spiel völlig außer Balance geraten würde, wenn alle Spieler einer Gilde beitreten würden, also müssten wir die Spieler zwingem, sich artig auf die Gilden zu verteilen. Schnappen sie sich aber gegenseitig wieder die Aufträge weg, verhindern sie gegenseitig den Gildenbeitritt. -->
> *Another problem: In the first sixth of the game, the player is not in a guild. He decides who he wants to join and makes admission tests. And these can only be made once. Which results in the same problem as above, 5 times as many missions.*  
> *More than that there is also the problem here, that the game would get completely out of balance, when all players would join the same guild, so we would need to force them, to politely distribute over the guilds. When they snatch the missions away from each other, they hinder each other from joining the guild.*  
<!-- Lösung: Den kompletten ersten Teil des Spiels im Multiplayer weglassen und jeden eine der Gilden über einen Auswahlscreen wählen lassen. Ihr seht worauf es hinausläuft? -->
> *Solution: To omit the complete first part of the game in the multillayer and let everyone choose one of the guilds in a selection screen. You see what this amounts to?*  

<!-- > Wir haben uns entschlossen den Multiplayer-Modus zu streichen, da wir ansonsten die Story nicht so hätten umsetzen können, wie geplant. Unser Ziel für den Multiplayer-Modus war es, die komplette Story spielbar zu machen. Doch bei der Umsetzung hätten wir leider viel zu viele Kompromisse zu Lasten der Dramaturgie und eines interessanten Storyplots machen müssen.
Den Multiplayer-Modus statt dessen als eine Art Deathmatch einzubauen, wäre auch keine Alternative gewesen, denn GOTHIC lebt von der Interaktion mit den NPCs, deren Reaktionen auf den Spieler, eben der lebendigen Welt in der man sich bewegt und mit der man auf sehr unterschiedliche Weise interagieren kann. -->
> *We have decided to cancel the multiplayer mode, because otherwise we wouldn't have been able to realise the story as planned. Our goal for the multiplayer mode was to make the complete story playable. But in the implementation we - sadly - would have to make way too many compromises at the expense of the dramaturgy and an interesting story plot.*  
> *To implement the multiplayer mode as a sort of Deathmatch instead also wouldn't have been an alternative, because GOTHIC lives from the interaction with the NPCs, their reactions to the player, just the living world through which one moves and with which one can interact in many different ways.*  

<!-- In den letzten Monaten hat sich gezeigt, daß es noch viele dieser Story- und Missions-Probleme gibt. Wenn man bedenkt, wieviel Zeit wir in die Lösung der ersten paar Probleme gesteckt haben, kann man sich ausmalen, wie lange es noch dauern würde, den Rest vernünftig hinzubekommen. Ich verstehe vollkommen, dass es für die Fans so rüberkommt, daß wir am Anfang mit Multiplayer-Storymode "geprahlt" haben und jetzt nicht halten können, was wir versprachen.  
Ich kann euch da draußen nur bitten, eine Sache zu bedenken: Die Entwicklung eines Spiels wie Gothic dauert in der Regel 2-3 Jahre. Und da ist es unmöglich am Anfang, als Newcomer Team mit einer handvoll Leute von vorneherein perfekt abzuschätzen, was in 2-3 Jahren geht und was nicht. --> 
> *In the last months it became obvious, that there are still many of these story- and mission-problems. When you consider how much time we have put into the solution of the first few problems, you can imagine how long it would take, to figure the rest out reasonably. I completely understand that for the fans it appears to be like this, that at the beginning we have bragged about a multiplayer-storymode and now we cannot keep our promise.*
> *I can only ask you out there, to consider one thing: The development of a game like Gothic usually takes 2-3 years. And it is impossible there, from the start, as a newcomer team with a handful of people, to estimate perfectly from the outset what is possible in 2-3 years and what not.*

----

### Critique of Impure Reason

**Flosha:** At first I will try to summarise the reasoning given. It boils down to the following problems:  

* Players can either not receive the same missions, have to just follow the main player or otherwise may take missions away from each other. 
* If not receiving the same missions, it would be too much work to write extra missions for each player. 
* Theoretical balancing issues due to the choice of a guild.

In my opinion, while all of the reasoning given makes sense and is understandable, it is (1) based on premises which are not in accordance with the vision of a storydriven immersive sim rpg and/or are (2) reasons which are only valid based on considerations of money (how much can be done in time while depending on funding of a publisher), which are no reasons of possibility, but only of efficiency. 

As for the problem of not being able to accept the same mission or taking missions away from each other: This is a problem that is only present under the conditions that every mission can only be accepted once. Mike describes two solutions: (1) Either not allowing the other players to get the mission, which would result in the need to have extra missions for each player, which he describes as a very bad solution. Or (2) only allowing the main player to get missions with all the other players following him in a party, as it is done in many "isometric" rpgs. But obviously there is a third solution, as it is done in many MMORPGs: (3) Just isolating the story and missions of each player from each other and enabling them to accept and solve the missions either independently from the other players *or* in a party (of e.g. two). In order for the players to not be in the way of each other by doing so, while still being in the same world, it would be needed to e.g. prevent the acceptance of a mission as long as another player or party of players are currently doing the mission. In consequence this would result in e.g. a scenario like this: Two players are accepting a mission to find the mages apprentice in the troll canyon. When the mission is solved (while the other players did something else), the same mission can be accepted by the third player which may or may not form another party with the fourth and/or fifth player, upon which the apprentice is spawned again and so on. It works. But it is the worst solution of all, that is opposed to the Immersive Sim the most.

But I will argue that all of this is irrelevant, looking at the problem from a wrong perspective. 

In his answers Mike gives the impression as if in the multiplayer there would be up to 5 players which are all on the same level, all convicted together, all without a guild and class and then developing their character at will. 

This approach is *of course* in conflict with the story. If the story is supposed to be believable, every character has to play a different role, have its own background story and so forth. It cannot be the same character (just looking differently) that is played by five players. It must be as it is in any good story-coop, where there are separate characters to be played. Never would or should a character say the same as another character or be told the same by NPCs as another character. The first solution, that Mike describes as very bad, is the only reasonable one. It is the only one that is in accordance with the design principles and the idea of a storydriven immersive sim rpg. 

And the story offered such individual characters: The five playable multiplayer characters should be the nameless hero and the four friends:

* `PC_PLAYER` (Hero)
* `PC_FIGHTER` (Gorn)
* `PC_MAGE` (Milten)
* `PC_PSIONIC` (Lester)
* `PC_THIEF` (Diego)

The four friends were convicted two years before the player, they already have a guild, a place in the prison hierarchy as well as an associated class, which solves all the problems regarding the first sixth of the game, by which Mike describes the first chapter.  
There is no need whatsoever to omit the first chapter, the only need is to think of the story from the individual perspective of the five characters.  


#### Character Selection

Before a multiplayer session, there of course has to be a character selection, where one of the players chooses the main hero, while others choose one of the four friends. If only two or three players play together, just one or two of the four friends turn into player characters, while the remaining friends remain NPCs like in a singleplayer session. 

The game starts regularly with the conviction of the main hero. The story, missions, dialogues and available answers for the main player are the same as in the singleplayer mode. 

The idea of enabling a friend to join a singleplayer session in the middle of a playthrough is easy from a gamedesign perspective (the technical implementation is a different question) insofar as that every one of the four friends has a clear scripted state and position in the game world etc. at any given moment of the story and can then easily be taken over at a specific point in time by another player joining the game. 


#### Fixed Roles

Exactly because of the story and in order to not compromise it, the other player characters are of course *not* possible to shape as much as the main hero, because they already have a fixed role. In the same way, as the main hero interacts with the four friends in the story, where they give specific answers, the possible dialogue options of the players controlling the friends have of course to be restricted. This is *not* a compromise, it is the opposite, it means *not* to compromise the story for the multiplayer, but to tell it consequently while allowing additional players to participate. 

Examples: A session starts. One player chooses the main hero, a second player chooses Diego. The main hero is being brought to his conviction at the cliff, while the player in control of Diego spawns on the way to the Cliff. Both characters have their individual mission logs. While the main hero is convicted and it will be his first task to orient himself in the colony (the first chapter being the "orientation phase"), Diego has a mission and motives of his own. 

While the main hero is baptised by the thugs, Diego can intervene. If he chooses to do so a dialogue with the main hero will be initiated, where the player character has the same dialogue options and Diego will say the same, in a fixed manner, as in singleplayer too. The player may then choose to accompany Diego as in 0.94k or to proceed on his own. In any way, the player will have to go through the story as known, will have to join a guild and so forth, while the four friends will have to play their own story. 

Just as with every other character in the game, we have to assume that the friends are *doing* their own stuff while the player character is doing his. The story implies this and the original story even more so. In this way, the main hero and the four friends are confronted with each other and crossing their paths several times in course of the story, things happen simultaneously and just as the main hero fulfills his role and takes part in driving the story forward or influencing it in some way or another, the friends too play an important role in the events.  

The old story implies that the four friends are meeting several times in course of the story. In the Alpha, Gorn and Lester are at the meeting place already at the beginning of the game and after escorting the player into the valley, Diego tells the player that he still has to do something. Later in the game, in course of the mission for Thorus of getting the list from the mine (it is not given by Diego), Diego seems to follow him and meets him in front of the mine, by the following dialogue and other, similar hints in the documents it is suggested that the four friends were meant to keep an eye on the main hero from the very beginning, they are working in the background, observing the player, talking about the events taking place in the colony and eventually helping him; while the main hero would form a stronger bond with one of the friends, depending on his choosen guild and/or class.

For example: In this particular case, the player is send to the mine for a mission to become a shadow (not given by Diego as it was done in the release version, where the same man who has stolen ore from the ore barons a few weeks ago is now suddenly the "leader" of the shadows; this is of course not the case). But in any way, Diego is a shadow himself and in the singleplayer campaign of the alpha story it is suggested that he follows him. For the multiplayer story for Diego we can derive a mission from here; such as an obvious solution like this: The leaders of the shadows is sending Diego to observe the player during the mission, which only makes sense: It is logical that a guild, which works similar to the Stasi of the German Democratic Republic, while training a new snitch, will of course have other snitches observing him at work in order to evaluate his loyalty and trustworthiness.  

So while being involved with the player, sometimes directly, sometimes indirectly, at the same time they would mind their own business: Lester for instance is involved in illegal drug trade, Gorn is a Mercenary, but has friends in the Organisation and is involved in their raids that are completely despised by Lee. Milten is doing stuff behind the back of his master Corristo and keeps meeting with his friends he is not allowed to see anymore.

They all have their story and thus telling these stories is the obvious solution for the multiplayer mode. While being linked to and taking place simultaneously to the events of the singleplayer plot, being part of that very plot, they each show the story from a different angle, tell additional stories in the world, develop the story further, give it more depth and complexity and provide answers to questions, such as: Why is Diego here, what brought him there, what did he do in the meanwhile, how does he relate to the other shadows? And so on and so on.

And since every character is experiencing his own story or the same story from his perspective with individual missions, these character plots could work just as well as additional singleplayer campaigns that can be played alone, in case of which the Main Hero would turn into an NPC and which guild he joins could be random, thereby always adding some element of surprise to a playthrough. 


#### Multiplayer Storytelling

Regarding dialogues, in the multiplayer mode every single dialogue would have to have an additional condition as simple as:

```
Player is PC_PSIONIC, then TRUE
```

Thus, depending on the character played, the NPCs would either talk to you or not and if talking to you they would only have dialogues specifically written with your particular character in mind. 

But the reader may realise a difficulty of this approach to a multiplayer story: When e.g. the role of Diego is taken by another player, how can one make sure that the main hero and Diego meet at the desired time? For example: When the player is send to the troll canyon and Diego is already there. How can this work, since the player in the role of Diego may be finished already before the main hero arrives? 

The answer is: In these particular cases, where two or more characters are supposed to be involved in a mission - which is the case in both the singleplayer and the multiplayer mode, the scenario has to be designed in such a way that the other characters are *needed* to solve the mission. There were missions supposed to be designed as such that one player alone cannot solve them. So a character cannot be finished here before another one is present. 

And as far as time is concerned: It is totally true that in a "player-driven" game as I called it, it would be very difficult to make sure that the story progression of two characters is in synchronicity *enough* to enable them to experience events together. But this is not the case in a real "[story-driven](/lore/driven-by-story)" game as I described it. Since the story is taking place on a day by day basis and most events will occur not earlier or later just because of the actions of the player character(s), the time at which an event occurs or the moment at which two or more characters are meant to meet to play together or to help each other, is clearly defined in a particular time frame, which in practice results in something like "Day 5 at Dusk". 

---

So, to summarise: It is only consequent, that the other characters do *not* receive the same missions as the main hero (in most cases), they have to be tailored specifically to one character, being influenced by his specific decisions. In some cases the friends *may* be able to solve a mission, that otherwise the hero would fulfill. For instance: If several thieves are looking for a particular artifact, Diego may do so too and get it before the player. But in no case can the very *same* mission be taken by several players (they may just  at most get an equivalent or a similar mission from the same or a different mission giver, but in a different context), nor can any player take a mission away from another, as it is never the very same. 

Just as there are missions that are written only for the main hero, there are missions only written for one of the four friends. 

And this may be a "shitty solution", to use Mikes words, due to the immense effort it takes, but it is the most consequent solution of the different multiplayer characters adds a lot of replay value. Every character plot tells the story of what they have done parallel to the player, how they were involved with NPCs in the world; they reveal and deal with many aspects which in the singleplayer main plot are only hinted at, that the player only hears about or even doesn't know anything about. 

---

### Summary

While speaking of compromises they didn't want to make with the story, for which they sacrificed the multiplayer, it is almost ironical, if it wouldn't be so unfortunate, that in the end they had to made more compromises with the story than in any other regard, as it was reduced in scope and depth so much while trying to rescue the project and sparing it from cancellation as a whole, that the result were much more serious sacrifices than the cancellation of the multiplayer. 

The (singleplayer) story of course has to have priority, as it is the base of everything. A multiplayer story can very well be realised and none of the problems explained above exist when following a consequent approach in accordance with our principles of a the storydriven immersive sim rpg. 

The developers had spend years with the development of the singleplayer story. In the end just a little fracture of the story they had developed could be implemented in the game as they had planned to. At the same time they have always said that the setting and this game world that they had devloped for such a long time and with so much passion and love for detail, is so rich and inspiring and that they had so many ideas left that they could have made several more games within this world. 

But instead of doing so and following such a passionate approach, instead of telling these stories (the only project going into such a direction (the Sequel) was cancelled and its developers fired), they have thrown all of these ideas out of the window and began to do something totally different in form of the official successors, into which not even half of that passion went into, as they would confirm themselves, nor were they even gothic-fantasy games. 

While from a historical perspective it was of course necessary to do all the cuts in the end as this was the only way that the game could be published that otherwise would have been cancelled the same way as its Sequel, - struggeling a lot already with the realisation of the singleplayer story alone - the stories of the four friends would have been ideal material for addons of the main game. 

Yes, for sure they wouldn't have been able to write these four additional side plots alongside the main plot in time, to release them alongside the main game, but there is no need to do so. In an ideal scenario, the multiplayer could have been developed one plot at a time, thereby expanding the Singleplayer story at first into a Multiplayer Story Coop for two players, then three, then four and finally all five, while at the same time giving the opportunity to patch the main game into a more complete state. 

And it also offers incredible incentives for the modding community. Because other than just telling new stories in different times and/or worlds, modders can make it their mission to create additional multiplayer characters for Phoenix, thereby always expanding the complexity of the story. What if you could play the story in the role of Xardas? What if you could play the story in the role of Scar? And so forth. 

And if the technical side of this endeavour is solved, - and there is work being done in that direction by programmers involved in Phoenix, among others - this is definitely the direction we would choose. Time will tell if this dream comes true. But it is clear, that the original Vision of Gothic will not be completely fulfilled without realising the Multiplayer Story Mode. 


## Freeplay Mode

Potential freeplay mode as known from STALKER utilising the entire game world, that could be opened up to a large number of players who would then be able to play their own stories here without a pre-narrated story, only with a simulated A-life, including occasional respawns of monsters, items, trading inventory updates and so forth. 

Freeplay could potentially be combined with a hardcore Permadeath Mode (the possibility of resurrection, as planned in the Alpha, which then would require help of other players, could make this more endurable); ans this could *also* be combined with the idea of switching into the role of any other random character in the gameworld, when the former one dies, so that every NPC can potentially turn into a player character.  

Many interesting ideas can be realised in such a mode. 


## Story Episodes

It would be possible to tell specific short story episodes which aren't taking more than 1-2 hours, like as events of the past, e.g. by giving the opportunity to play two convicts helping each other during the revolt, such as the barons themselves. 


## Additional Modes

* **Arena:** Battles in various smaller or larger, literal or metaphorical "arenas" from the game. Arena may be played in multiplayer in form of Deathmatch (1vs1), in form of team deathmachy (e.g. 2vs2), in Coop against hostile NPCs or even in Singleplayer against NPCs, in which case the Arenas serve as well as practice of the combat/magic system in general.  

* **Survival:** Fight agaimst waves of enemies to survive  (e.g. survive against human opponents or against harder and harder monsters in the Arena, survive against the Orcs in the Outside Ring, survive against the Revolt in the Castle, survive against the Madmen at the Pass etc.); the waves may have a fixed number or may be endless with the potential of player rankings by the maximum time they manage to survive.  
 
These modes may be possible to be played with various multiplayer characters that have to be unlocked in story mode (as well as the arenas themselves). 

