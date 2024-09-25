# Multiplayer

``Author: Flosha``  
``25.09.2024``

From the very beginning of the development, Gothic had always been promoted as having a multiplayer. It was an essential part of the project that they wanted to realise, mentioned in every interview and several times did let it seem that they are actually proud of the concept behind their multiplayer, which was meant to be different than what players knew at the time. 

``Add quotes``

It was meant to be playable by 5 to 8 players (the announced numbers always varied in course of time) and only in local networks via LAN (online was too slow at the time).  

``Add quotes``

But then, somewhen in 1999, after 3+ years already had been spend to realise it, it was announced that the multiplayer has been cancelled by the developer. 

We will at first deal with the reasons for the cancellation which were explained in detail by Mike, before offering a critique of that reasoning from our perspective and in the context of our design philosophy. 


## Reasons for the Cancellation

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

----

## Critique of Impure Reason

**Flosha:** In his answers, Mike gives the impression as if in the multiplayer there would be up to 5 players which are all on the same level, probably all convicted together and then developing their character at will.  
But the multiplayer was based on the idea of one nameless hero and the four friends. The four friends are convicted already, they already have a guild and a place in the prison hierarchy as well as an associated class. 


Darum ist die konsequenteste und zugleich die interessanteste Lösung eine Kombination von 1 und 2. Es ist nur konsequent, dass die vier Freunde in vielen Fällen NICHT die Missionen erhalten, die der Held bekommt, die sind auf ihn als Charakter zugeschnitten und abhängig von seinen Entscheidungen. In einigen Fällen KÖNNEN die vier Freunde eine Mission erfüllen, die andernfalls der Held erledigen könnte; in keinem Fall aber kann dieselbe Mission von mehreren Spielern angenommen werden. 

Die Lösung ist also simpel:
Einige Missionen funktionieren wie beschrieben in seiner Lösung 2: Die vier Freunde oder einer davon wird in manchen Fällen eine Mission mit einem anderen Spieler zusammen erledigen, die dieser angenommen hat. Andere Missionen müssen aber, wie in Lösung 1 beschrieben, exklusiv auf die jeweiligen Charaktere zugeschnitten sein. Genauso wie es also Missionen gibt, die nur der Held erhalten kann, so gibt es Missionen, die nur einem der vier Freunde gegeben wird basierend auf dem jeweiligen Charakter. Es mag eine "Scheißlösung" sein aufgrund des großen Aufwands, den das bedeutet. Aber es ist die konsequenteste Lösung, die zudem durch die spezifischen Storystränge der verschiedenen Charaktere im Multiplayer zusätzlichen Wiederspielwert bedeutet.
Ja, es ist mehr Aufwand, aber man hätte sich z.B. auf die Umsetzung der Hauptstory für den Helden konzentrieren können und dann die vier Freunde in vier kleinen Addons für den Multiplayer nachliefern können, die die vier Freunde in die Hauptstory einflechten und ermöglichen, in ihre Rolle zu schlüpfen und dem Spieler zu helfen bzw. zu erleben, was sie parallel zu dem Helden getan haben, was man im Singleplayer nur erzählt bekommt oder gar nicht weiß. 

Weiter mit Mike:

---

Noch ein Problem: Im ersten Sechstel des Spiels ist der Spieler in keiner Gilde. Er entscheidet sich, wem er beitreten will und macht Aufnahmeprüfungen. Diese können auch nur einmal gemacht werden. Also schonmal dasselbe Problem wie oben, 5 mal so viele Missionen.
Darüber hinaus gibt es hier aber noch das Problem, dass das Spiel völlig außer Balance geraten würde, wenn alle Spieler einer Gilde beitreten würden, also müssten wir die Spieler zwingem, sich artig auf die Gilden zu verteilen. Schnappen sie sich aber gegenseitig wieder die Aufträge weg, verhindern sie gegenseitig den Gildenbeitritt.
Lösung: Den kompletten ersten Teil des Spiels im Multiplayer weglassen und jeden eine der Gilden über einen Auswahlscreen wählen lassen. Ihr seht worauf es hinausläuft?

---

Flosha: Auch das ist kein Problem. Da im Multiplayer nur einer der namenlose Held sein kann werden die anderen in die Rolle eines der Freunde schlüpfen. Die sind aber schon in einer Gilde. Aufträge, die relevant für einen Gildenbeitritt sind, können sie sich also nicht wegschnappen.

---

Wir haben uns entschlossen den Multiplayer-Modus zu streichen, da wir ansonsten die Story nicht so hätten umsetzen können, wie geplant. Unser Ziel für den Multiplayer-Modus war es, die komplette Story spielbar zu machen. Doch bei der Umsetzung hätten wir leider viel zu viele Kompromisse zu Lasten der Dramaturgie und eines interessanten Storyplots machen müssen.
Den Multiplayer-Modus statt dessen als eine Art Deathmatch einzubauen, wäre auch keine Alternative gewesen, denn GOTHIC lebt von der Interaktion mit den NPCs, deren Reaktionen auf den Spieler, eben der lebendigen Welt in der man sich bewegt und mit der man auf sehr unterschiedliche Weise interagieren kann.
In den letzten Monaten hat sich gezeigt, daß es noch viele dieser Story- und Missions-Probleme gibt. Wenn man bedenkt, wieviel Zeit wir in die Lösung der ersten paar Probleme gesteckt haben, kann man sich ausmalen, wie lange es noch dauern würde, den Rest vernünftig hinzubekommen. Ich verstehe vollkommen, dass es für die Fans so rüberkommt, daß wir am Anfang mit Multiplayer-Storymode "geprahlt" haben und jetzt nicht halten können, was wir versprachen.
Ich kann euch da draußen nur bitten, eine Sache zu bedenken: Die Entwicklung eines Spiels wie Gothic dauert in der Regel 2-3 Jahre. Und da ist es unmöglich am Anfang, als Newcomer Team mit einer handvoll Leute von vorneherein perfekt abzuschätzen, was in 2-3 Jahren geht und was nicht.
