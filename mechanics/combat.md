# Combat Mode

*Flosha, 28.09.2024*

* Critique of the Combat System
* Controls
* Combat Skills
  * Fistfighting (Hand to Hand)
  * Swordfighting (1H/2H)
  * Battle Axes
  * Spears
* Combat HUD



## Critique

*28.08.2024 - 28.09.2024*

At the beginning we will quote everything of relevance about what the fighting system was meant to be according to interviews and design documentation. Then we analyse how this compares to the actual implementation in the game. In the end we present our own solutions. 

> Alex: *Gothic is a real-time game. Combat will also be real-time, but for the biggest part it won't depend on your trigger finger if you succeed or fail in a fight. For example there will be no way for you to kill an enemy with a full plate armor and a battle-axe if you are bare-handed, except sneaking from behind and pushing him over the ledge. Fighting in Gothic will have strong tactical elements. Do I attack, step back, or parry the enemy's blow and start a counter-attack?*  
> *You can actually plan your next moves because our combat system doesn't rely on fast reflexes. If you want to be totally defensive, then you can keep your weapon up by pressing a key, and you will parry every blow that your opponent does. You just have to take into consideration that if the attacking force is much stronger than you - you can't parry a two-handed weapon with a dagger - you will be pushed back or even can fall to the ground. If you're more into fighting from a distance, you could use bows or crossbows. Depending on your talent, you will be able to aim at fast moving targets or you can try to do a critical hit by aiming at your enemy longer.* - [rpgvault.ign.com 06/1999](https://gothicarchive.org/interviews/1999/29.06.1999_rpgvault.ign.com.txt)



## Parade System

17.04.2023

Based on the document by Alex Brüggemann, we know that while they always have spoken of "Parade", it actually has always been nothing but a block. It was about blocking in the right moment or even just...

> *If you want to be totally defensive, then you can keep your weapon up by pressing a key, and you will parry every blow that your opponent does.* [I]

At the same time the combat system was described as being tactical. But the only tactical considerations in the Alpha was which weapon to use against which monster or how else to get rid of it, if not by means of combat (e.g. distraction). They wanted it to be very simple and fun, but at the same time did not want it to rely on any reflexes but it should primarily depend on his stats (attributes) only. I think that this a wrong premise. The combat system of Morrowind relies entirely on stats and is the opposite of fun. 

The Fighter related Attributes in PHOENIX make it *possible* to use a weapon (effectively) and the Combat Skills give the character additional movement options or more speed etc. to use in combat, but being an action-rpg there should still be a system in place, that actually requires the player to learn and improve alongside his character. Requiring some reflexes is not a bad thing; "easy to learn and hard to master" was a goal that they themselves had originally for the gameplay in general, but in how they implemented their combat system that never really became a reality. Unless one considers constant backing off or running around enemies in circles as tactical, fun and "hard to master". But in Mikes original concepts there *was* more to it, and all the available unused alpha animations can help us understand these concepts better.
 
So we want more tactics here. But we stick to the idea of limiting ourselves to the ~10 keys they planned having due to the number of keys of gamepads at the time, for which Gothic has been optimized from the very beginning, while *not* being meant to be played with a mouse. 

Therefore we will start by considering the direction keys and what the Alpha is offering animation wise. Among the unused Animations, we clearly can differentiate thst there was not only a "basic" hit and then a blow from left to right and right to left, but there were essentially four kinds of attacks based on directions: Left to right, right to left, from a raised position downwards and from a lowered position upwards. These four "directions of attack", as we may call it, we can link with the direction keys.  

The later fighting skills will always consist of these basic directions of attack, they will just be faster and animated differently, apart from a few turns and special attacks. But these we will preserve for "Combos" (these combos one can apply upon a successful parade).

Jeder NPC und der Spieler hat demnach mit 1H Waffen diese vier möglichen Angriffsrichtungen und genau so muss auch die Parade passieren. Also wenn der Gegner dir gegenüber steht und von rechts nach links schlägt, dann musst du im richtigen Moment einen Schlag nach links ausführen, also in die Richtung, aus der er von dir aus gesehen kommt, um seine Attacke zu parieren.
Wenn er von oben runter schlägt, musst du von unten nach oben ausholen um den Hieb zu parieren. Wenn er von unten hoch schlägt musst du von oben runter.


David: Wie stellst du dir dann die Steuerung dafür vor von oben nach unten und von unten nach oben zu schlagen?
Hätte man dann erstmal eine Möglichkeit, die Waffe in eine bestimmte Richtung auszurichten und müsste dann den Angriff ausführen?

Flosha: Also in der Alpha ist ja die Kampfpose etwas anders, man steht erstmal neutral, wenn man ein Schwert zieht. Genauso wie wenn man steht, wenn man jetzt einfach nur ein Schwert aufhebt und in der Hand hat. Durch Gedrückt halten von CTRL nimmt man die Kampfpose ein. Auf dem Gamepad wäre das wohl R2 oder sowas. 
In dieser Kampfpose wird das Schwert dann nach vorne gehalten bzw. abhängig von deinem 1H Level ändert sich die Kampfpose.

Diese Pose nochmal bewusst anpassen zu können und eine andere einzunehmen würde es glaube ich zu kompliziert machen. Wenn dann vielleicht über eine Taste, dass man einfach zwischen drei Posen oder so durchswitchen kann auf Knopfdruck, die dann auch erstmal so bleibt bis man sie manuell ändert, dadurch könnten Spieler ein wenig individuell stehen im Kampf. Aber die Grundidee ist, dass du aus dieser Standardpose heraus alle Schläge in die vier Richtungen ausführen kannst (also z.B. links-rechts Schläge gehen ja jetzt auch schon im Spiel egal aus welcher Pose heraus). Manche Posen mögen vielleicht besser sein, um bestimmte Schläge auszuführen, weil man sonst weiter ausholen muss, so dass sehr geübte Spieler dann durchaus auch zwischendurch mal die Pose ändern könnten, um noch effektiver zu reagieren, aber möglich soll es aus jeder Position heraus sein.

Steuerung für Schläge nach oben oder unten: Pfeiltaste nach oben oder unten. Bzw. der Steuerknüppel auf dem Gamepad. Um Kombos auszuführen bzw. stärkere Attacken sind dann manchmal Tastenkombinationen nötig, zB. einmal schnell hintereinander "Pfeil runter Pfeil hoch" um extra stark auszuholen und nach oben zu ziehen (dabei denke ich zB. an eine Ani aus der Alpha).

+
Das mit den Tastenkombinationen ist nur für Spezialattacken, also man kann auch ohne die erfolgreich kämpfen, und wenn man nicht gut parieren kann, dann kann man auch zurückweichen, Schlagen, zurückweichen etc. Aber je besser man wird je eher kann man direkt in den Gegnerkontakt gehen, parieren und dann Spezialmoves ausführen.

Bei den Spezialmoves stell dir Tony Hawk's Pro Skater vor. Kann man auch durchspielen ohne Spezialtricks, aber es gibt mehr Punkte und ist extrem befriedigend wenn man es schafft Spezialtricks zu machen. Dafür muss man im richtigen Moment Tasten drücken. Meistens einfach nur zwei Tasten in ner bestimmten Sequenz schnell hintereinander. Und um das zu tun hat man den kurzen Moment nach erfolgreicher Parade, wenn der Gegner gestunned ist.
Würde ich dann vllt. wirklich auch mit einem (jedoch dezenteren) Soundeffekt unterlegen, wenn man einen Spezialmove schafft, das sorgt dann für dieses "Yea, Special Move!"-Gefühl.

+++
Ich denke dass dieses vier Richtungssytem die richtige Mischung ist bzgl. Taktik und Herausforderung ohne all zu komplex zu werden wie jetzt vllt. in Kingdom Come oder so (noch nicht gespielt). Am Anfang ist man selbst und die ersten Gegner ja langsamer, so dass man auch mehr Zeit hat um auf Schläge zu reagieren und in die richtige Richtung zu blocken. Außerdem kann man das ganze in unserem Demo Level üben, der dann auch als eine Art Tutorial Level dienen kann, den man im Menü abrufen kann um sich mit den Mechaniken vertraut zu machen.

Und wenn man es dann später mit Gegnern wie etwa Scar zu tun bekommt, dann schlägt der halt richtig schnell und das Zeitfenster in dem man reagieren muss ist sehr viel kleiner.
So wird zwar der eigene Charakter besser, stärker und schneller, man muss aber auch selbst besser kämpfen lernen.

Es wäre halt auch mal was anderes, wie es vllt. noch nie umgesetzt wurde. Es ist immernoch arcadig, aber hat trotzdem einen gewissen Grad Realismus.

Wichtig damit das gut funktioniert ist, dass sich das ganze Kämpfen direkter anfühlt, die Reaktionszeiten usw., die sollten sich im Laufe des Spiels verringern. Immoment sind die zu lang. Am Anfang geht es vielleicht noch gerade so, aber am Ende muss es sich viel direkter steuern.

Ich denke dass man zuerst die wichtigsten Anis reinbringen muss und dann diese grundlegende Parademöglichkeit, dass dann ein Gegner, je nach Richtung, unterschiedlich zurückgeworfen wird. Das wiederum kann dann aber auch von Stats abhängen. Also wenn zB. Scar auf dich einschlägt und du bist nur halb so stark wie er, selbst wenn du dann super schnell bist, falls du das überhaupt schaffst, kann es dann immernoch sein, dass sein Schlag trotzdem durch kommt und die Parade nicht erfolgreich ist. All diese Dinge muss man dann halt feintunen.

Und dafür brauchen wir dann wohl neue Anis, für Gegner, die aus verschiedenen Richtungen pariert wurden und dann ein-zwei Schritte zurückweichen müssen oder dergleichen. Dieses gestunned sein und so.

David: Ich find die Idee sehr gut. Macht das ganze definitiv mehr skill-basiert und auf jeden Fall nicht so eintönig wie im Original, wenn sowohl der Spieler als auch die Gegner die Richtungs-Attacken einsetzen können und man die Parade jeweils spielerisch erstmal lernen muss und sich die Gegneranimationen dafür merken muss. Man muss sich dann also für das Parieren die Attacken von den Gegnern anschauen und je nach Skillstufe der Gegner verringert sich dann die Reaktionszeit, weil die Gegner schneller angreifen. Da wirds dann auch mit der Skillstufe auch schwieriger die Spezialattacken einzusetzen, weil man immer kleinere Reaktionszeitfenster kriegt. Klingt auf jeden Fall sehr spaßig, aber auch nach ner Menge Rumprobieren, bis es richtig passt. :D

Wenn CTRL+Pfeiltaste nach unten ein Schlag nach unten ist, gibts dann noch Blocken?

Flosha: Ich denke es macht ja eh keinen Sinn so richtig zu "blocken" mit einem Schwert, meistens ist es ja eher der Versuch den Schlag des Gegners wegzulenken durch einen eigenen Schlag. Das klassische Blocken könnte vielleicht immernoch passieren aber dann zB. als die Parade für Schläge von oben wenn man noch schwach ist oder als Block eines Spezialangriffs oder man integriert es als Gedrückt halten nach unten statt schneller Druck für die Parade oder irgendsowas. Aber generell würde ich das ganze Blocken eher gesondert angehen wenn es Richtung Schildkampf geht, falls wir das einbauen.
Oder vielleicht Doppelt Pfeil nach unten für einen Block

Mit diesen Tastenkombinationen (ich hoffe sehr das ist möglich, sowas einzubauen dass du schnell zwei Tasten drücken musst und er das dann richtig und schnell checkt und ne Spezialmove ausführt) wollte ich auch die Akrobatik realisieren.

Zum Beispiel: Wenn im Gehmodus oder wenn Shift gedrückt, dann macht man einen Präzisionsprung. Also auf der Stelle springen mit zwei Füßen auf ne andere Stelle, für Platforming etc. Wenn im Laufmodus macht man den normalen Sprung nach vorne. Hat man Akrobatik Stufe I gelernt wird kein Sprung ersetzt sondern man kann die Flugrolle machen durch Sprung + Doppelt Pfeil Nach Oben

Wenn man im Kampf ist macht man mit Alt und Pfeil zurück nen Ausweichhüpfer rückwärts. Mit Akrobatik würde man dann mit ALT + Doppelt nach hinten nen Flic Flac machen oder so. Später Salto etc.


David: Mit Union sollte das auf jeden Fall möglich sein. Man kann abfragen, in was für einer Animation sich der Spieler oder ein anderer NPC befindet in der DoAi Funktion, die wird jeden Frame ausgeführt für jeden NPC und dann könnte man einen Timer laufen lassen und die Inputs von bestimmten Tasten abfragen und schauen, in was für einem Zeitabstand die Tasten jeweils gedrückt wurden. Damit sollte sich ne Menge machen lassen.
Man müsste durch Rumprobieren nur stark schauen, dass das nicht clunky ist und das sich das einfach richtig anfühlt von den Zeitabständen und den Animationen. Also sowohl bei der Akrobatik als auch beim Kämpfen.

David: 
Wie wäre das dann eigentlich mit normalen Angriffen? Man nimmt dann verschiedene Posen ein? Mit einer Pose kann man normale Angriffe wie im Original-Spiel machen und mit anderen Posen dann die Kombis?

Flosha: Warte. Also nochmal:
Wenn man die Waffe zieht soll man erstmal nur so rumstehen normal mit Waffe in der Hand wie bei jedem anderen Item. Man steht dann so da wie man auch da stehen würde wenn eine Waffe auf dem Boden liegt und man die aufhebt. Dann hat man die auch einfach in der Hand wie ein reguläres Item und kann sich dann entscheiden sie wegzustecken oder wieder fallen zu lassen etc. Das ist wie es jetzt schon bei uns funktioniert über Auronens Item-Handling Plugin.

Erst wenn man dann STRG gedrückt hält, nimmt der Spieler eine Pose ein.
Die Pose, die dann eingenommen wird, wäre erstmal automatisch vorgegeben und abhängig vom Skill-Level, so wie im Originalspiel auch (wo es je nach 1H Skill zB. drei verschiedene Posen gibt oder so plus die als ungeübter).

Während diesem Halten der Pose kann man dann mit den Richtungstasten (wenn wir jetzt von der Tastatursteuerung ausgehen) Angriffe ausführen.
In Vanilla ist es dann ja so dass man hauptsächlich nur von links nach rechts, von rechts nach links und nach vorne schlagen kann.
Bei uns soll es so sein, dass man von links nach rechts, von rechts nach links, aber auch von oben nach unten und von unten nach oben schlagen kann. Und so soll man dann auch schlagen müssen abhängig von der Attacke des Gegners. 

Schlägt der Gegner dich von dir aus gesehen von rechts (und angenommen du weichst nicht aus), dann musst du auch einen Schlag nach rechts machen um seinen Angriff zu parieren. Schlägt er von oben runter, musst du von unten nach oben schlagen um sein Schwert in diese Richtung zu parieren. Also immer sozusagen ihm entgegen kommen, so wie auch im Faustkampf, wenn du dir Wing-Chun oder so vorstellst, wo halt von irgendner Richtung die Faust kommt und du dann deine Bewegung nutzt um diesen Angriff wegzulenken.

Und die "Spezialattacken" die mit diesen speziellen Tastenkombos ausgeführt werden sollen, also dass man drei oder vier Tasten schnell hintereinander drückt z.B., die sollen funktionieren wenn sozusagen dein, nennen wir es jetzt mal "Fokus"-Meter aufgeladen ist im Kampf, oder deine "Berserker-Bar", whatever. Also stellen wir uns vor, man kann durch Kampf, durch erfolgreiche Paraden in einem Kampf und angebrachte Schläge dieses Spezialmeter aufladen (wie die Spezialtrick-Leiste in Tony Hawk als Beispiel) und sobald das voll ist und die Spezialattacke zur Verfügung steht (das muss nicht tatsächlich in einer Bar angezeigt werden sondern kann auch unsichtbar oder simpler und immersiv angezeigt werden, aber nur zum Verständnis), dann sollen diese Tastenkombis funktionieren.

Also das heißt, da wäre dann keine andere Pose nötig, es wäre derselbe Kampfmodus nur dass durch diese aufgeladene "Special-Bar" die Special-Tastenkombinationen ausführbar werden. Und diese Special-Bar würde sich durch erfolgreiche Paraden auffüllen innerhalb eines laufenden Kampfes und durch erfolgreiche Schläge, während sie durch Treffer abnimmt oder so oder sogar völlig geleert wird; so dass man eben angehalten ist möglichst sauber zu kämpfen, immer zu parieren, aber auch nicht zu defensiv zu sein und nur auszuweichen, weil man auch dadurch die Bar nicht aufladen kann. Und wenn sie einmal voll ist bleibt das gelocked und sie bleibt dann für ein paar Sekunden voll solange man nicht getroffen wird. Oder vielleicht auch wenn man durchaus getroffen wird und schon kurz vor 0 hp ist, so dass man so noch einmal einen Befreiungsschlag ausführen könnte, das könnte auch cool sein.

David: Unterbrechen die Kombis dann einfach die Animation vom normalen Angriff oder gibt es da dann eine Wartezeit, wann ein Angriff ausgeführt wird? Die Kombis brauchen ja einen gewissen Timeframe, also die Tasten müssen ja innerhalb einer bestimmten Zeit gedrückt werden, man will ja aber auch gleichzeitig, dass das Kämpfen schnell ist und man direkt auch angreifen kann.

Flosha: 
Hm. Ja das sind so Details, ich weiß nicht wie man das am besten implementiert. Wenn ich mir jetzt Tony Hawk vorstelle, das ist ja auch alles sehr sehr schnell. Und man fährt da rum und wenn man jetzt nen Spezialtrick machen will, dann drückt man die Tasten ja super super schnell hintereinander, weil man ja nicht sonderlich viel Zeit hat in der Luft bevor man wieder auf dem Boden landet und da muss der Trick ja schon wieder vorbei sein. So stell ich mir das vor, dass der Spieler normal am Kämpfen ist, am parieren usw., dass er sieht: Yes, jetzt ist mein Focus Meter voll und das er dann einen günstigen Moment abpasst, ala: "Okay, noch einmal eine Parade, das stunned den Gegner kurz und dann hau ich voll rein." Dass er also erst seinen Angriff zuende führt, dass er Zeit hat den Spezialschlag anzubringen und dann drückt er schnell die Tastenkombi und done. 

Wenn er das natürlich irgendwie macht während er gerade schon in einem anderen Angriff drin ist.. Eine Lösung dafür wäre folgende: Kombos gehen nicht aus dem Nichts, sondern als Connections nach einem Standard-Schlag. Also Beispiel es gibt die "Super-Duper-David-Schlag-Attacke". Und die kann man NUR machen nach einem Schlag nach oben. Dann wäre es ähnlich wie bei den Standard-Kombos im Spiel. 
Eine andere Kombo geht NUR nach einem Schlag nach rechts zB. Dann würde der Spieler immer erst einen Standard-Schlag machen, hätte dann da dieses kleine Zeitfenster, wo die Waffe in der richtigen Position liegt nach diesem Schlag und von dort aus kann er die Spezialattacke anbringen, die sich dann optisch gut dort einfügt.

---
Auronen hat mir eben erzählt, dass Mark56 an einem Directional Block Feature arbeitet.
Das ist scheinbar in etwa genau sowas wie ich es geplant hatte, aber ohne es zu wissen ist das wohl so schon im Spiel angelegt.

```
zSTRING oCAniCtrl_Human :: GetHitDirection()
{
    zCModelAniActive* hitAni = GetModel()->GetActiveAni(hitAniID);
    if (!hitAni) return "O";
    
    return zSTRING(char(comboInfo[comboNr].comboDir));
};
```


David: 
Du hattest ja vor allem Pro Skater im Kopf mit den durchführbaren Kombos, aber ich bin mit Tekken 4 aufgewachsen und hatte das z.B. gar nicht auf dem Schirm, denn das ist nen Arcade Game, wo man genauso Kombos hintereinander einsetzen muss, aber gleichzeitig auch mit Gegnern interagiert, im Tekken Force Mode sogar mit ganz vielen gleichzeitig.

Nice, ist gut, wenn es mehrere Ansätze gibt und er da auch alleine was auf die Beine stellt, was man am Ende nutzen kann. Ich habe immer den Andrang, wenn ich etwas umsetze, es so multifunktional wie möglich zu machen. Ich bin da viel zu ambitioniert. Ich würde das Kampfsystem z.B. gerne mit dem Split-Screen implementieren und somit mit Kampfpartner mir das System spielerisch erarbeiten, sodass die Gegner möglichst glaubwürdig wie der Spieler selbst im Kampf funktionieren, das ist mir sehr wichtig, weil es so am meisten Spaß macht gegen Gegner zu kämpfen, denke ich und ich es so auch bei eigenen Projekten nutzen könnte. Das ist bei der Tekken KI, und bei allen anderen Fighting Games auch, ja z.B. so. Wenn ich erstmal so etwas auf die Beine gestellt habe, kann ich es dann auch viel leichter für dich individuell anpassen, dass es dann auch genau so funktioniert, wie du es haben willst.

Flosha, feedback
Tekken 4 Force Mode Video:
Was ich daran sehr mag ist die Perspektive. Ich finde dass wir so eine seitliche Perspektive zumindest bei Faustkampf haben sollten. Das passt einfach und in der Alpha war das ja teilweise auch so drin. Bei Schwertkampf würde ich keine komplett seitliche sondern so eine etwas diagonale Perspektive wählen, wie es in den späteren Alphas auch noch war oder hier in diesem Tekken Video.

Mir ist auch neulich aufgefallen, dass das in Enter the Matrix auch so gelöst wurde. Da gibts ja auch viel Nahkampf/Kung Fu und da wechselt die Kamera dann immer in diese seitliche Perspektive, während beim Schießen die Kamera in der Third Person Behind-The-Shoulder Kamera bleibt.

---

Ein anderer kleiner Faktor, der mir dabei mal aufgefallen ist, ist was einen Unterschied das machen kann, wenn es unterschiedlich große Charaktere gibt. In Gothic ist ja fast jeder NPC gleich groß. Hier gibt es teilweise deutliche Unterschiede. Wenn man zB. den Kampf bei Minute 2 anschaut, Morpheus und Agent Smith, wirken die richtig groß, mal verglichen mit Niobe am Anfang. Und irgendwie gibt ihnen das auch ein ganz anderes Gefühl von Gewicht und Bedrohung. So ein bisschen mehr Größenunterschiede bei Charakteren in Gothic wär denke ich ne gute Sache. Wenn man dann mal einem menschlichen Gegner gegenübersteht, der einen Kopf größer ist oder so, wirkt das direkt viel einschüchternder.

 allein die Größe schüchtert da schon ein und man meint man ist unterlegen. Auch im Gothic Comic wurde ja sowas eigentlich auch angeteasert. Da kämpft ja Orik gegen irgendnen anderen, der ist auch ein Riese und Orik ziemlich klein im Vergleich.

---
Ist natürlich viel rudimentärer als in Tekken, aber es ist ein Beispiel für ein Spiel wo imo der Wechsel zwischen den beiden Kameraperspektiven je nach Spielsituation sehr gut funktioniert und sich auch gut angefühlt hat.

David: Was ich gerne umsetzen würde in Gothic, ist, wie man mit den Gegnern um sich herum kämpft mit den Combos, die man ausführt und wie die KI tickt. Die KI analysiert deine momentane Kampfposition und nutzt dann einen Move, der dir Schaden macht oder sie schaut, welche Attacken du einsetzt und wehrt sich dementsprechend, sie macht aber natürlich auch absichtlich Fehler, damit du überhaupt in Stande bist, gegen sie zu kämpfen. Du kannst in Tekken ja entweder normal stehen, ducken oder springen, nach hinten gehen oder ducken und nach hinten schleichen, Tekken 4 hat da noch den Seitwärtsschritt, damit man um einen Gegner herumlaufen kann, hinzugefügt und da gibt es Low, Middle, High und das Ausrufezeichen als Angriffe. Ausrufezeichen durchbricht die Haltung des Gegners immer, aber dafür muss man eine Combo halt perfekt beherrschen, damit der Angriff überhaupt zustande kommt und darf währenddessen auch nicht unterbrochen werden, muss also schauen, dass keine anderen Gegner nah bei einem sind und der Gegner vor einem auch in der richtigen Position ist, dass man überhaupt zum Angriff kommt. Ich mag einfach die Schwierigkeit daran sehr, dass man die Combos erst lernen, perfekt timen und beherrschen muss und nicht einfach irgendwelche Tasten spammen darf. Ist halt sehr skillbasiert und es macht auf Dauer auch sehr Spaß. Bei Gothic ist das mit dem Timing und dem taktischen Gameplay ja auch ähnlich, aber zu simpel und zu schnell zu meistern. Das ist hier einfach, und bei Fighting Games allgemein, nicht so.






## Combat Skills

### Fistfighting





## Combat HUD

...
