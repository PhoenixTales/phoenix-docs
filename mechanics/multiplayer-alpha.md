# Alpha Multiplayer

``Author: Flosha``  
``Created: 25.09.2024``  
``Last update: 25.09.2024``  

---

**Content:**
* [Multiplayer Concepts](#multiplayer-concepts)
* [Reasons for the Cancellation](#reasons-for-the-cancellation)
* [Critique of Impure Reason](#critique-of-impure-reason)

---

## Multiplayer Concepts

From the very beginning of the development, Gothic had always been promoted as having a multiplayer story mode (which we call "Coop" today). It was an essential part of the project that they wanted to realise, mentioned all the time in interviews:

> Tom Putzki: [...] we've planned to give at least 8 Multiplayers the chance to compete in Gothic. (11.06.1998)

> Mike Hoge: [...] we want to make a network game. (15.06.1998)

While at first they have spoken of "at least 8" players, this was changed very soon to 5, a number with which they sticked till the end. 

> Gibt es einen Multiplayer-Modus?  
> Tom Putzki: Aber klar doch! Zusammen mit seinen Freunden und Kollegen ein richtig gutes Spiel zu zocken, bringt doch noch mehr Fun als alleine vor dem Rechner zu hängen. (01.05.1999)

> g0mp: Gothic ist kein reines Online Spiel wie UO, kann man trotzdem mit einer Netzwerk Option oder dergleichen rechnen?  
> Tom: Sorry, Internetversion von GOTHIC ist derzeit nicht in Planung... zumindest nicht bei der derzeitigen Anbindung in Deutschland - Lags...(( aber Multiplayer ist selbstverständlich, bis zu 5 Spieler im lokalen Netzwerk....und als besonderes Leckerchen: Die Story ist sowohl im Single- als auch im Multiplayer kontinuierlich spielbar!!!! (01.05.1999)

Most players may not know or remember much of what the Gothic multiplayer was meant to be, but for how little of it had actually been implemented in the game the developers promised a lot of specific details about the multiplayer in 1998-1999.  
 
> How is Gothic going to support Multi-player? Will you be able to adventure with your character build up in single player along with your friends favorite characters?  
> Mike: Yes. But we plan to allow only characters of the same level to join a game, to keep the game balance intact. As we started with GOTHIC, I imagined a game where you can play several hours in single player mode, then join a game with your friend and take your character with you and finally even take the improvements you`ve made in your multiplayer session back to your single player game...  
> Tom: Just to explain: GOTHIC is divided into six chapters, and you can only join a game, if your characters are in the same chapter. (20.06.1998)

They also claimed that the way that the multiplayer would be realised in Gothic is something new that has never been done (most likely referring to the goal of letting players seemlessly take their character back and forth between Single- and Multiplayer): 

> Stefan Nyul: We figured out a very smart design for the multiplayer mode. This will be something absolutely unique, never done before. But let us finish the implementation before talking of details.
   
> Tom Putzki: What can be said right now is the fact that GOTHIC can be played in a local network with up to five players. And about this unique feature I want to say... [he didn't say more] (14.11.1998)

> Mike: In the multiplayer game you can play through the whole story with up to 5 players. Its no deathmatch, although you can kill the other players if they let you :). Making the multiplayer game work the same way the singleplayer game does is in my eyes a unique feature many people will hopefully enjoy (and that btw cost us hell lots of design time). Compared to Online RPGs we have small player numbers, but a complex story and many living characters to explore... 
(16.10.1999)

As you see, the two interviews quoted above are almost a whole year apart. In October 1999 the multiplayer was still in the making, at that point since 1997. 

But very shortly after this, after 2-3 years had been spend with the feature, at some point at the end of 1999, it was announced that the multiplayer mode has been cancelled by the developer.  

We will at first deal with the reasons for this cancellation which were explained in detail by Mike, before offering a critique of that reasoning from our perspective and in the context of our design philosophy. 

``TODO: Add additional details e.g. regarding the Resurrection or Teleport system from the documents.``


## Reasons for the Cancellation

``Source: gothic.gomp.ch, 1999``
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
1. Spieler B bekommt die Mission nicht - alle Missionen dieses Strangs müssen von Spieler A gemacht werden - Scheißlösung, denn wir müssten uns bei 5 Spielern 5 mal so viele Missionen einfallen lassen.
2. Einer der Spieler bekommt immer alle Missionen, und die anderen müssen ihm "unfrei" als Party folgen -> Problem: Jeder möchte gerne Missionen annehmen können.
UND: So würden immer alle Spieler überall gemeinsam hinlaufen. (Das wiederum ist ein weiteres Problem) -->

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


## Critique of Impure Reason

**Flosha:** At first I will try to summarise the reasoning given. It boils down to the following problems:  

* Players can either not receive the same missions, have to just follow the main player or otherwise may take missions away from each other. 
* If not receiving the same missions, it would be too much work to write extra missions for each player. 
* Theoretical balancing issues due to the choice of a guild.

In my opinion, while all of the reasoning given makes sense and is understandable, it is (1) based on premises which are not in accordance with the vision of a storydriven immersive sim rpg and/or are (2) reasons which are only valid based on considerations of money (how much can be done in time while depending on funding of a publisher), which are no reasons of possibility, but only of efficiency. 

As for the problem of not being able to accept the same mission or taking missions away from each other: This is a problem that is only present under the conditions that every mission can only be accepted once. Mike describes two solutions: (1) Either not allowing the other players to get the mission, which would result in the need to have extra missions for each player, which he describes as a very bad solution. Or (2) only allowing the main player to get missions with all the other players following him in a party, as it is done in many "isometric" rpgs. But obviously there is a third solution, as it is done in many MMORPGs: (3) Just isolating the story and missions of each player from each other and enabling them to accept and solve the missions either independently from the other players *or* in a party (of e.g. two). In order for the players to not be in the way of each other by doing so, while still being in the same world, it would be needed to e.g. prevent the acceptance of a mission as long as another player or party of players are currently doing the mission. In consequence this would result in e.g. a scenario like this: Two players are accepting a mission to find the mages apprentice in the troll canyon. When the mission is solved (while the other players did something else), the same mission can be accepted by the third player which may or may not form another party with the fourth and/or fifth player, upon which the apprentice is spawned again and so on. It works. But it is the worst solution of all, that is opposed to the Immersive Sim the most.

So, how could we implement a real multiplayer story mode? 

I will argue that all of the points made before are irrelevant, as it is looking at the problem from a wrong perspective. 

In his reply Mike gave the impression as if in the multiplayer there would be up to 5 players which are all on the same level, all convicted together, all without a guild and class and that every player should have been able to develop their character at will; the four friends in the Alpha Multiplayer should thus be seen only as *prototypes* of what the multiplayer characters could potentially be developed *into*.

This approach is *of course* in conflict with the story. If the story is supposed to be believable, every character has to play a different role, have its own background story and so forth. It cannot be basically the same character (looking differently, but being interacted with by NPCs all the same), that is played by five players. And in this case it is of course totally unreasonable to develop five times as many missions to enable every one of these characters to experience the story in his own way while actually meant to be the same, as Mike imagined everyone to be the hero and no one with a fixed role. It is this premise that leads to all of the problems. 

While speaking of compromises they didn't want to make with the story, for which they sacrificed the multiplayer, it is almost ironical, if it wouldn't be so unfortunate, that in the end they had to made more compromises with the story than in any other regard, as it was reduced in scope and depth so much while trying to rescue the project and sparing it from cancellation as a whole, that the results were much more serious sacrifices than the cancellation of the multiplayer. 

The (singleplayer) story of course has to have priority, as it is the basis of everything. But a multiplayer story can very well be realised and none of the major problems explained above exist when following a consequent approach in accordance with our principles of a storydriven immersive sim rpg. 


### Read next

* [Phoenix Multiplayer](/mechanics/multiplayer-phoenix)


<style>

    main {
        background: url("/_img/bg/code.jpg");
        background-position: top right;
        background-size: 80%;
        background-repeat: no-repeat;
        width: 100%;
    }

</style>