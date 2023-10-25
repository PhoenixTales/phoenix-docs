# Phoenix Attributes 


**Author:** Flosha  
**Status:** <span class="changed">Work in progress</span>  

Based on our research of the [Alpha Attributes](/mechanics/attributes-alpha), in this second part, we will present our own solution for Phoenix, how we reconstruct the old attributes and how we develop the relevant concepts further.  


## Content  

1. [Reconstructing the Attributes](#reconstructing-the-attributes)
    1. [Primary & Secondary Attributes](#primary--secondary-attributes)
        1. [Strength, Constitution, Hitpoints](#strength-constitution-hitpoints)
        2. [Dexterity, Hitchance & Risk](#dexterity-hitchance--risk)
        3. [Will, Psi & Madness](#will-psi--madness)
    2. [The Arts](#the-arts)
        1. [Psionics](#psionics)
        2. [Arcanery](#arcanery)
        3. [Weaponry](#weaponry)
        4. [Thievery](#thievery)
    3. [Arts <> Attributes Correlation](#arts--attributes-correlation)
        1. [Attribute Scaling](#attribute-scaling)
2. [Attribute Progression](#attribute-progression)
    1. [Phoenix' Default Values](#phoenix-default-values)
3. [Phoenix HUDs](#phoenix-huds)
    1. [Enhanced Symbol HUD](#enhanced-symbol-hud)
    2. [Enhanced Bar HUD](#enhanced-bar-hud)
4. [Beyond the HUD](#beyond-the-hud)
    1. [Possession](#possession)    
5. [Summary](#summary)


## Reconstructing the Attributes

In the past when we only had access to the list of alpha attributes (from the `worldfile.txt`) without any context and without any of the related documents or alpha demos and builds that we analysed above, we could only guess their meaning.  

We didn't know about Mikes early idea of a "black soul" bar, we didn't know for sure about a relation between Madness and Will, about Mikes handwritten attribute lists and of the correlation of different attributes. All these insights were only made possible by our [rescue of the design concepts](https://phoenixthegame.com/specials/20thAnniversary/) that we digitised and published in the Archive. And yet we had come to very similar conclusions on our own.  

At first and influenced by the release system I imagined that there was some difference between attributes such as Strength, Dexterity, Hitpoints, Mana, Willpower (as the Mana equivalent for Psionics; that much we knew from the interviews), to things like Arcane, Swordsmanship and Thievery. Following the original german terms (*Waffenkunst*, *Diebeskunst*) I conceived them as "Künste" (Arts) mostly relevant for the specific skills of the four classes, in opposition to the main attributes relevant for all. With the little problem that there was no fourth "art" that we would have been able to assign to the psionic player. Will, while surely being of special importance to the psionic, we imagined to be of general importance to all (since we imagined it to be of importance as a resistence against psionic powers and the psi emissions with the madness waves) and we didn't know about the correlation and the confusing difference (primary and status attribute) between Will and "Willpower".

Thus, the arts were defined by me as pre-requisites for class-specific skills ("talents") to learn and I came up with the idea of the Arts as a specific form of experience that would reward the player for using the skills of his chosen class, all in order to reinforce the story-driven gameplay and at the same time to replace the general experience points, which, as various early statements suggest (see [Experience](/mechanics/experience)) we deemed to not have been part of the initial vision of the game. It gave sense to the "arts" and was a neat little system to overcome any form of grinding.  

Another idea of mine that is not grounded in any research was to combine Strength and Hitpoints; the details of which we will explain below. But in short: I liked the simplicity of it, I was inclined to it for how it deviates from the usual system in RPGs and due to the interesting balancing.  

But since all the attributes were just mixed up in the scripts the main aspect that we only became aware of through the acquisition and research of the design documents was the difference of first and second order attributes and their correlation that we now had to consider and to explain.  


### Primary & Secondary Attributes

In their striving to finish the game it might have been reasonable to remove the "first order" attributes, but based on how they were the initial idea, since they were part of the concept for so long and due to their strong correlation with the classes - which to fully realise is one of our primary goals - and how their remnants inspired our imagination for years, we will have to reconstruct the "first order" attributes. We will find good reasons for them to persist and we will equip them with meaning in context of the setting as well as for gameplay.

In order to do so we have to analyse the difference between those attributes which are relevant for all classes and those which are optional or even mutually exclusive.  


#### Strength, Constitution, Hitpoints 

Constitution is relevant to everyone and with no primary focus on any class. Strength is primarily relevant and skilled by Warriors. Mages and Psionics may not skill it at all, but it is nonetheless a factor that matters to every character; it sets limits of how you can or can not interact with the world (as in form of carrying or pushing objects). And therefore everyone will have some degree of Strength.  

But strength is *not* needed anymore as a requirement to equip weapons, but it is needed to handle weapons effectively; both melee and ranged weapons. Handling a heavy sword while being too weak to handle it effectively results in fast or immediate exhaustion, and drawing a strong bow or crossbow may not be possible at all, as that requires quite a bit of strength too. Both are visualised by animations.

Strength and constitution have to be closely interlinked. Strength will scale the `DP` (damage points) to some degree (100% in fist fighting, 50% in melee combat, 0% in ranged combat - here it is the weapon alone that defines the damage), as originally planned, but constitution will not scale the `HP` (hit points). `HP` and `DP` represent the damage that the character can inflict and the damage he can endure. Mana and Willpower according to Alex' description define both magic and psi damage *as well* as the resistance against magic and psi. Why shouldn't this be the case for strength too?  

Damage (as scaled by Strength in the sense of force output) will diminish by a factor of 0.5 with decreasing hitpoints, but the strength value itself will not diminish (with a few balancing and story related exceptions).

So in our system, while both strength and constitution exist internally and will be referred to by NPCs, one who can deal more damage can automatically endure more damage and vice versa. Your overall physical "Kraft" (strength) defines both. Thus it is the Strength that scales both hit points and damage points, while Constitution is correlated with *regeneration* - of energy (hit points) as well as of (strength-)endurance. Endurance is the ability of the organism to withstand exhaustion and the ability to regenerate from stress. Thus the endurance value defines how long a character can sprint and how fast he reaches full exhaustion. Less `HP` result in faster exhaustion. 

In our system, someone who has more strength can also endure much more hits. But at the same time the regeneration takes longer and requires more energy, while for someone with low strength but high constitution, the regeneration is faster and requires less energy. In the same way someone with less strength (and therewith less body mass) can sprint longer and higher constitution results in faster regeneration of the sprinting meter (displayed like the oxygen bar).  

Additionally, endurance will influence fatigue. The character fatigues if he doesn't sleep for long. The fatigue of the character will have the result that he does not regenerate energy (hit points) automatically anymore. The automatic regeneration works as long as there is fuel in form of food being eaten regularly and as long as there is not too much fatigue accumulated. This way we do not force anyone to eat, drink or sleep as some survival games do, but we *reward* him if he does. One can as well play without the automatic regeneration, can heal himself by different means. Just in order to have the full advantage of regeneration one has to eat some food and sleep. 

Endurance is insofar connected with it that a high endurance expenditure between two sleep cycles has an increasing effect on the accumulation of fatigue. In effect this means: You have to sleep more in order to maintain your regeneration if you sprint/fight more. 

And there is another particularity: When the endurance is exhausted the player will be able to continue sprinting. But at that point he slowly starts to loose his energy (hitpoints). In this way one can sprint until collapsing. In some cases this might be important, for instance if one has to flee from a monster. Obviously the exhaustion after sprinting *past* the normal endurance has to be displayed by an extra animation. Also important: Endurance is the only attribute that is improved in a pure *learning-by-doing* way.

The `HP` regeneration will be so slow (slower than the mana regeneration and *way* slower than the endurance regeneration), that it will not be too useful in battle (if not suspended completely). Herbs and potions that greatly speed up regeneration will therefore remain meaningful. By this and other changes we take care that all the items in the game have some relevance for the player. 

If both the endurance and the hitpoints are exhausted to some degree, the hitpoints will always regenerate first and the endurance second. The endurance bar is like a buffer that one has before what is done will wear one's energy out ("an seinen Kräften zehren"). Healing is never immediate. It happens always through regeneration; where the automatic regeneration is slowest and the regeneration by magic and HP potions is fastest. 

* `ATR_Strength` -> `ATR_Hitpoints` + `DMG` 
* `ATR_Constitution` -> `ATR_Endurance`, `REG_HITPOINTS` + `REG_ENDURANCE`


#### Dexterity, Hitchance & Risk

Dexterity, in opposition to strength, is not a primary attribute (as seen by its absence in the attribute levels in clear text form). It is a secondary attribute that is scaled by thievery and serves the purpose of being displayed as DEX symbols in the Icon HUD. Other than that it influences the "hit chance" in ranged combat and the "risk of failure" in stealth. 

* `ATR_Dexterity`


#### Will, Psi & Madness 

How about Will? In the way that Will was planned and used in the Alpha, it was solely associated with psi magic and protection against the same. *Only* psionics had any amount of Will, everyone else had none at all and they would only be protected against psionic magic via psi-protective armor pieces, amulets and so forth.  

We think that this is not convincing and more importantly, that it greatly misses all the other ways in which we can utilise Will in the game world. Before we knew anything on how the attribute was supposed to function in the Alpha, Arbax imagined that the willpower of NPCs and the player character would also be important in dialogues; the psionic would not just use spells, he also could use speech to intimidate others, he could force his Will on others by words and depending on their own Will they would be able to resist or give in to such attempts.  

And the same for such things as control. When the psionic attempts to control an NPC success should depend on his Will being stronger than the Will of his opponent. And this is as it was actually planned in the earliest docs by Mike. In various notes on spells he wrote how the success of a spell depends on the enemies Willpower.  

The values as they were distributed in 0.94k seem not to be consistent with this idea. In Phoenix every NPC will have some amount of will and NPCs of higher levels should automatically have higher Will. But how can that be the same as the "willpower" in the sense of the psi energy, of which Y'Berion has to have most among the humans and the Sleeper himself must have an abundance of?  

Here we come to the meaning and importance of the Will and Psi-Energy correlation. Only psionics should have Psi-Energy; that is what they themselves refer to as "Willpower", but that is in reality a kind of demonic force. This Willpower is what is left in 0.94k (which, as we should remember, only contains the "secondary" attributes) and in this sense it makes sense how non-psionics have no amount of Willpower (= Psi). Every NPC should have some amount of *Will*, but it should not be confused with the *Willpower* of the psionics. And since these two terms continue to cause confusion, we will refer to Willpower as *Psi-Energy* from now on.  

The correlation of Will and Psi-Energy is that while someone with a strong Will may not have any Psi-Energy, someone with Psi-Energy (or psi-power-potential) will automatically have more of it when he has a strong will; his Will determines his maximum *potential* Psi-Energy.  

Example: Gomez will have 10 Will but 0 Psi.  
Y'Berion will have 10 Will but 30 Psi.  

Will is a primary attribute of which 10 levels exist for everyone. Psi is a correlated and class specific attribute that has to be acquired in course of the story by joining the sect.

```
+--------------+
| Will | ≤ Psi |
|------+-------|
| Lv1  |     3 |
| Lv2  |     6 |
| Lv3  |     9 |
| Lv4  |    12 |
| Lv5  |    15 |
| Lv6  |    18 |
| Lv7  |    21 |
| Lv8  |    24 |
| Lv9  |    27 |
| Lv10 |    30 |
+--------------+
```

In this way, the level of Will determines the *potential* of psi-energy usage before drifting into madness.

<p class="subtext">For monsters, psi is scaled by factor 2.<br>
Thus, the Sleeper at Lv10 has 60 Psi.</p>

At the same time it is Will that controls the *resistance* against Psi.  

But we also have to consider Madness. Here we are confronted with the two contrasting approaches that are mostly about representing madness or sanity in the HUD. Will is an absolute value that cannot be diminished. Psi-Energy has an actual and a maximal value that can be exhausted and recharged. And there are two kinds of Psi:  
One is the Psi-Energy handled by a psionic and represents the maximum amount of demonic force a psionic can handle. The other is the environmental Psi-Energy in form of psi emissions, in form of localised psi-rays at so called "psi-knots" and in form of the general psi-radioactivity in the atmosphere which increases in course of the story and from emission to emission. 

<p class="subtext">While the Psi-Energy of Psi-NPCs is automatically scaled by their Will from 0 to 30, player characters have to find Psi-knots in the game world to increase their Psi-Energy.</p> 

The Psi-Energy of the psionics can be fend of by enough Will. The localised psi-rays can be avoided by keeping distance from psi knots or external protection. But the psi emissions and general radioactivity past a certain point can only be endured by drugs or strong external protection.

The condition that most NPCs won't have any access to such drugs anymore nor any kind of psi protection - while the psi forces in the environment keep being increased - will be the primary reason for the *Nemesis* - another example for how consequent we interlock the game mechanics with the story; more on that in the Alpha Story documentation. But without a dedicated madness value independent from the psionic-exclusive Willpower, nothing about that could be displayed in the game as originally intended.  

Based on these ideas, it is simply not sufficient to have Will as described before and the psi points as exclusive energy of psionics like mana points as exclusive energy of mages. Madness cannot be the lack of the primary Will attribute, since that is an absolute value, nor can it be just the lack of Psi-Energy; if 0% Psi would equal 100% Madness everyone but the psionics would be mad and a psionic player could never fully exhaust his available Psi-Energy. Thus, the Psi-Energy or Willpower that is psionic-exclusive can not equal the Sanity or Madness meter that should be relevant to all NPCs.  

We assume that this complex relation and interconnection, while it may vaguely have been at the back of ones head, was never properly documented, it was confusing and thus was confused in the actual implementation in the engine and the alpha builds. We attempt to dissolve this confusion.  

In consequence there arises the need to add Madness *additionally* and *independently from Psi*, where another of my old concepts comes into play that I developed in the end of 2018:

Madness as negative Willpower.  

That said: The Will of an NPC protects from Psi attacks and thus from Madness -> since attacking someone in the psionic way basically means to drive him mad. But at the same time, dealing with Psi-Energy in such a way is dangerous. As Tom Putzki told us, quoting one of his favourite lyrics from Rammstein: *"Der Wahnsinn ist nur eine schmale Brücke"* (Madness is just a small bridge). But more correctly I would say: Sanity is a small bridge, Madness lies beneath and the psionic is always on the edge...  

We will not let psionic casting "automatically end" as the early note by Mike suggests, instead it will become a gameplay factor for the player to know the mental capacity of his character and to be on or close to this edge and decide how much he can lean beyond.  
When he deals with the energy beyond his treshold (when all Psi-Energy points are used up or when the psi bar is fully discharged), the Madness (in form of the black soul bar or new dedicated madness symbols) begins to fill.   

While it is safe to say that this was never actually planned as such and that this is our original solution that we came up with just based on the terms Will and Madness before knowing about the concepts behind it, it may actually be the only way in which we can include both the Psi-Energy discharge as implemented in the game and the "black soul bar" idea of increasing Madness from Mikes concept; our solution combines and harmonises both.

Thus, in this context we need the following attributes:  

* `ATR_WILL` 
* `ATR_MADNESS` 
* `ATR_MADNESS_MAX` 
* `ATR_PSI`
* `ATR_PSI_MAX`



### The Arts 

It may be that the "arts" were removed because they wanted to simplify a system that had become too complicated. They may have become redundant because of how they developed the skill system. If we include them, we will not include them as attributes but as a category on their own. In the same way as `PROT` was introduced as a dedicated constant of protection values, we will introduce `ART` as a dedicated constant of the arts. But we do that *only* if thereby we make the system not more complicated, but more interesting and reasonable. Otherwise they're only useful as categories of skills, as headings in the character sheet.  

One purpose of the arts in our system is to serve as concepts that can be verbalised and described inside of the game world by NPCs (as well as books and so on) to seperate them from the abstract status attributes, which only play a role for the HUD and for the internal calculation of specific forms of damage, resistance and so forth. 

Our solution is to include the arts as a requirement for the learning of skills, in the sense of the acquired knowledge or artistry or "specific experience" in an art that a teacher requires the character to have in order to teach him. So, for instance, Corristo will not ask for your level, your "LPs" or "EXPs" (both of which do not exist anymore), but he will ask for your knowledge of the arcane, for your specific, art-related experience. 

The arts serve as over-arching categories of skills and represent no general but a specific experience of the art in question, as the requirement for learning higher levels of skills.  

Additionally, their function is to serve as class-specific forms of experience to reinforce what we coined as "learning by acting". The player is being rewarded by playing in accordance of his chosen class, by consequently acting out his role in the game. More about this concept in our document about Experience. But in short: Experience is specific and thus having experience in one specific art does not serve as a requirement to learn unrelated skills, while there is still some amount of carry-over, e.g. the experience in weaponry gained by One-Handed Combat carries over to the ability to learn combat in other weapon categories.  

The warrior strives to master combat and weaponry. The thief strives to become a master thief, to master thievery. The mage strives to dive into the arcane knowledge and to reach the highest initiations. And we will add an additional art: "psionics", as will be explained below.  

"Hitchance" in combat and "risk" in stealth (of being caught, of breaking a lockpick etc.) are influenced by Weaponry and Thievery respectively. Combat specific skills (such as One-Handed Combat Level 1-3) do not influence the purely internal hitchance, but they affect agility, speed (in form of faster animations) and reaction (by influencing the input-delay).

```
     +------------------------+
     | Künste      | Arts     |
+----|-------------|----------|
| DK | Diebeskunst | Thievery |
| WK | Waffenkunst | Weaponry |
| AK | Arkanei     | Arcanery |
| PK | Psionik     | Psionics |
+-----------------------------+
```

Weaponry signifies the experience in Combat.  
Thievery signifies the experience in Stealth.  
Arcanery signifies the experience with Magic.  
Psionics signifies the experience with Psi Magic. 

---

#### Psionics

While in the alpha research we correlated Arcane, Weaponry, Thievery and Will to the four classes, Will does not really fit into this scheme and our proposed system. It wouldn't be consequent due to how important Will is for every character and independent of the class compared to Thievery and Weaponry that are clearly class focused.  

One approach would be to argument that while the psionic magic and the alchemical magic are completely independent, *Arcane* may work as an overarching attribute of magical knowledge for both magical classes. But that doesn't fit because one of the essential characteristics of psionics in classical roleplaying games is exactly their despise of the "Arcane" that stands for the traditions and rituals of the clerics (here of the cults of the realm with the mages as priests).  

Thus, either we would have to go without a psionic equivalent to the three Arts for the other classes (which would be inconsequent) or we have to come up with something more suitable to the heretic nature of the psionics (which would be consequent and is obviously what we do). Thus, we will add "psionics" as an art.  

In the same way as the arcane art opens the mind and prepares the body of the mage for the Mana, a psionic art has to open the mind and prepare the body of the psionic to the Psi-Energy. Opening the mind and preparing the body for the Psi-Energy means to enable him to see or sense this energy in the first place (such as in form of the psi-knots) and to learn handling it. So what this psionic art has to be about is not the Arcane, but a psychic or mystic sense.  

Just as the mage can lead the way to the magical ore (that he needs for his potions which again he needs to boost Mana) due to his ability to alchemically sense physical substances that are magically charged, having a whole set of additional perceptions unknown to those without the *Arcane Gift* (more about these concepts of ours in the documentation of the Magic Mode and Magic in the lore section), in the same way there are additional perceptions to the highly skilled psionic, opening up a world beyond the physical and allowing him a glimpse into the mystical, psychical (or demonic) reality like an overlay over the world perceived by others, by which, for instance, he can see the psi-knots that he needs to boost his maximal Psi-Energy and other phenomena.  

The psionic brotherhood (which was highly inspired by Buddhism in fact), uses the sign of the open / opening eye. And obviously the open eye signifies awakening. That is exactly what the psionic art has to be about, what they all are working on: to awaken. The psionic strives to awaken himself and thereby the sleeper and to awaken the sleeper and thereby himself; one through the other. 


#### Arcanery

Arcanery is the experience and knowledge of the Arcane. It is increased through teaching from masters in the art, through reading arcane books and through acting according to the chosen class as a mage (using magic to solve game situations). It is indicated by the "circle" of the mage - his level of initiation - and at the same time the experience in the arcane serves as a requirement to receive said initiations.  

The Arcane Art does not really matter to anyone but the mages, but one may still acquire a bit of arcane knowledge by chance - as the psionics may steal knowledge from the mages and so on. The important thing is that they won't get any Mana (due to intoxication) -> Mana is mage exclusive, as Psi-Energy is psionic exclusive.  


#### Weaponry 

Weaponry is primarily relevant for warriors. It is increased through teaching from experienced fighters in the combat forms with different (melee) weapons and through applying said teachings in combat. At the same time every teaching in a specific weapon's combat form requires X experience in Weaponry. 


#### Thievery

Thievery is obviously relevant for thieves and while thieves may be able to reach some degree of Weaponry (his dagger-tricks are thief-skills and thus not associated with Weaponry), it is the thievery that he is primarily supposed to use to solve the game. It is increased through teaching from experienced thieves and through applying said teachings in stealth. On the other hand, it also serves as a class-specific experience requirement for additional teachings. Thus, every thief skill to be learned in the game comes with a different requirement in Thievery. Thereby, the character can only be developed as a thief by solving game situations in accordance with the thief's abilities as his class-specific repertoire of interaction.  



### Arts <> Attributes Correlation

Thievery <> Dexterity  
Weaponry <> Strength  
Arcanery <> Mana  
Psionics <> Psi

Every art scales an associated status attribute. 


#### Attribute Scaling

Thievery scales Dexterity, Weaponry scales Strength, Arcanery scales the ability to boost Mana permanently (which otherwise would result in intoxication) and Psionics scales the ability to collect more Psi-Energy. 

Additionally there are a few cases of mutual influence between attributes. (Physical) Strength scales Will automatically by a factor of ~0.5. And reverse: Increases in Will scale Strength by a similar factor. 
 
In this way we simulate how a warrior gains mental strength too in course of his physical training and how high Willpower can have an effect on physical strength. At the same time it solves a balancing problem, in that it enables warriors to focus on strength development while still increasing their resistance against psionic attacks, and templars to increase their Willpower without missing out on too much gains in strength. 


### Attribute Progression

Every art comes with ten levels. There are 10 possible levels of primary attributes and class-specific experience. Based on the incomplete and work in progress texts from v0.56c, we come up with a complete structure for the ten levels of attributes analysed before (and those added by us). The list is <span class="added">work in progress</span>. All the names written in white are original, those marked in green were changed, the ones in red did not exist and were added.  

<pre>
|    | Kraft          | Konstitution     | Wille          | Waffenkunst   | Diebeskunst    | Arkane Gabe | <span class="added">Psionik</span>      |
|----|----------------|------------------|----------------|---------------|----------------|-------------|--------------|
|  1 | gelähmt        | <span class="changed">halbtot</span>          | <span class="changed">besessen</span>       | keine         | keine          | <span class="added">keine</span>       | narkotisch   |
|  2 | schwindsüchtig | komatisch        | willenlos      | wehrlos       | unbeholfen     | <span class="added">Kreis 1</span>     | schlafend    |
|  3 | schwächlich    | kränklich        | willensschwach | unsicher      | tollpatschig   | <span class="added">Kreis 2</span>     | träumend     |
|  4 | schwach        | <span class="changed">anfällig</span>         | unsicher       | wehrhaft      | ungeschickt    | <span class="added">Kreis 3</span>     | fantasierend |
|  5 | kräftig        | robust           | <span class="added">zaghaft</span>        | treffsicher   | geschickt      | <span class="added">Kreis 4</span>     | eingekehrt   |
|  6 | stark          | widerstandsfähig | <span class="added">gefestigt</span>      | <span class="changed">sehr behände</span>  | fingerfertig   | <span class="added">Kreis 5</span>     | durchbrochen |
|  7 | bärenstark     | athletisch       | entschlossen   | Meister       | meisterhaft    | <span class="added">Kreis 6</span>     | geblendet    |
|  8 | unbezwingbar   | zäh wie Leder    | unbeugsam      | ...           | Fingerkünstler | <span class="added">Secret</span>      | versunken    |
|  9 | <span class="added">Secret</span>         | <span class="added">Secret</span>           | <span class="added">eisern</span>         | ...           | ...            | <span class="added">Secret</span>      | erleuchtet   |
| 10 | <span class="added">Secret</span>         | <span class="added">Secret</span>           | <span class="added">frei</span>           | <span class="added">Schwertsänger</span> | ...            | <span class="added">Secret</span>      | erwacht      |
</pre>

That said, based on the principle of "immersion by visualisation" a character with 1 or 2 strength should be so weak and exhausted that this weakness can clearly be *seen* in his animations. And based on the principle of "immersion by verbalisation" we will ideally have no need for a "print", when the experience of the player is not sufficient (while of course it remains possible to do that, optionally, if the purely descriptive system is not seen as expressive enough). When, for instance, the player wants to learn a thief skill from Fingers, but has not gained enough experience in Thievery yet, Fingers will refer to the player's experience directly in the dialogue (by the descriptions the player knows from the character sheet). When he is internally on level 5, which in the character sheet is described as *dextrous* ("geschickt"), he lacks one level before being *nimble-fingered* ("fingerfertig"). In this case Fingers would tell him something like: "You are *dextrous* indeed, but not yet *nimble-fingered* enough..." In this way there will be no need for printing any numbers on the screen. This is reasonable in regard to immersion, because the character you play does not know anything about some numbers representing his "values"; what he knows is how he feels. The terms above are a reflection of this condition.  


#### Phoenix' Default Values

The Status Attributes in Phoenix with our before mentioned necessary additions will consist of the following values. 

```
  Range of Values per Species						
+-----------------------------------------+
| Attribute       |  HUM  |  ORC  |  MON  |
|-----------------+-------+-------+-------|
| Hp  | Hitpoints |  5-30 | 15-45 |  ≤100 |
| Str | Strength  |  1-15 | 10-30 |  1-50 |
| Dex | Dexterity |  1-15 |  1-10 |  1-10 |
| Wil | Willpower |  0-15 | 10-25 |   ≤50 |
| Mad | Madness   |  0-15 |  0-25 |   ≤50 |
| Man | Mana      |  0-30 |     0 |     0 |
| Psi | Psi       |  0-30 |  0-40 |  ≤100 |
+-----------------------------------------+
```

The values are divided into light, medium and heavy default presets for NPCs, where heavy serves as the upper maximum of values for a given class of NPCs and light as the minimum; values can be fine-tuned individually for balancing within this set framework.  
The attributes that are not listed in a class are zero (0 Mana for Warriors and so on). Madness is zero at game start for all but will progress in course of the story; for this we implement a specific madness function triggered by global events. These are the default preset values in Phoenix: 

```
  Workers
+-----------------------+
| ATR |  L  |  M  |  H  |	
|-----+-----------------|	
| Hp  | ≤10 | ≤14 | ≤18 |
| Str |  ≤5 |  ≤7 |  ≤9 |
| Dex |  ≤3 |  ≤5 |  ≤7 |
| Wil |  ≤0 |  ≤2 |  ≤4 |
+-----------------------+
Exception Novices: 
  Str |  ≤2 |  ≤4 |  ≤6
  Wil |  ≤5 |  ≤7 |  ≤9
  Psi |  ≤2 |  ≤4 |  ≤6


  Warriors (E = Orebaron) 			  Thieves (T = Masterthief) 
+-----------------------------+		+-----------------------------+
| ATR |  L  |  M  |  H  |  E  |		| ATR |  L  |  M  |  H  |  T  |
|-----+-----------------------|		|-----+-----------------------|
| Htp | ≤18 | ≤22 | ≤26 | ≤30 |		| Htp | ≤18 | ≤22 | ≤26 | ≤30 |
| Str |  ≤9 | ≤11 | ≤13 | ≤15 |		| Str |  ≤4 |  ≤6 |  ≤8 | ≤10 |
| Dex |  ≤4 |  ≤6 |  ≤8 | ≤10 |		| Dex |  ≤9 | ≤11 | ≤13 | ≤15 |
| Wil |  ≤4 |  ≤6 |  ≤8 | ≤10 |		| Wil |  ≤4 |  ≤6 |  ≤8 | ≤10 |
+-----------------------------+		+-----------------------------+
Exception Templars: 
  Str |  ≤6 |  ≤8 | ≤10 | ≤12
  Wil |  ≤9 | ≤12 | ≤15 | ≤18
  Psi |  ≤6 |  ≤9 | ≤12 | ≤15


  Mages (A = Archmages) 			  Gurus (Y = The Enlightened) 
+-----------------------------+		+-----------------------------+
| ATR |  L  |  M  |  H  |  A  |		| ATR |  L  |  M  |  H  |  Y  |
|-----+-----------------------|		|-----+-----------------------|
| Htp | ≤18 | ≤22 | ≤26 | ≤30 |		| Htp | ≤18 | ≤22 | ≤26 | ≤30 |
| Str |  ~5 |  ~5 |  ~5 |  ~5 |		| Str |  ~5 |  ~5 |  ~5 |  ~5 |
| Dex |  ~5 |  ~5 |  ~5 |  ~5 |		| Dex |  ~5 |  ~5 |  ~5 |  ~5 |
| Wil |  ≤6 |  ≤9 | ≤12 | ≤15 |		| Wil |  ≤6 |  ≤9 | ≤12 | ≤15 |
| Man | ≤15 | ≤20 | ≤25 | ≤30 |		| Psi | ≤15 | ≤20 | ≤25 | ≤30 |
+-----------------------------+		+-----------------------------+

```


### Phoenix HUDs

The HUD will be optional and it will be possible to play without (see ["Beyond the HUD](#beyond-the-hudbeyond-the-hud) below). We will provide both the symbol HUD and the v0.8 bar HUD as options in the menu. We use improved versions of both of them and you can toggle them on or off. We hide the HP Bar/Symbols by default in the exploration mode when not wounded.  

The following attributes or other values will be displayed on the screen:
* Hitpoints (when injured, in Combat Mode or in the inventory)
* Exhaustion/Oxygen (when sprinting or diving)
* Mana (when in Magic Mode or in the inventory)
* Psi (when in Psi Mode or in the inventory)
* Madness (when having any amount of madness points)

The following values are exclusively displayed in the Icon HUD:
* Strength (when in Combat Mode or in the inventory)
* Dexterity (when in Stealth Mode or in the inventory)
* Damage (when highlighting weapons in the inventory)
* Protection (when highlighting armor pieces in the inventory)


#### Enhanced Symbol HUD

Sasha (aka Jr) was inspired by the Symbol HUD of the alpha versions and started to develop an enhanced version of it. There was no symbol to represent oxygen when diving, so he added a little bubble symbol. Since he imagined that one symbol such as HP does not necessarily correlate to one health point internally, but may be the sum of a specific number of healthpoints, he included an optical transition. As we know now one symbol should exactly correlate to one health point, such that this idea has become redundant.  
In cooperation with me he later improved the HUD even further and designed it to our liking; he included the possibility to switch between the Symbol- and Bar-HUD from the menu, provided options to customise the HUD to ones liking and included Phoenix presets (such as hiding HP when not injured).  

In order to not have 30 icons on the screen, we will have 3 levels represented by "cooler", "reinforced" symbols, such as in my exemplatory concepts below.   

The first screen shows life points of level 2 (dark red) and 3 (purple) as well as mana points of level 2 (blue / golden) and 3 (dark blue & red):  

![Corristos HUD example HP & MP Level 2+3](/_img/mechanics/HUD/HUDCor.png)

This screen shows life symbols of level 1 (default) and 2 and Psi-Energy / Willpower symbols of level 1 (default) and 2 (darker, glowing eyes, open mouth):  

![Psi HUD example Level 1+2](/_img/mechanics/HUD/HUDPsi2.png)

Based on an idea by Alex mentioned in the documents, we also add new strength symbols for different species, such as these concepts for Gobbos and Orcs; other creatures such as Lurkers and Scavengers will receive more differentiated ones, obviously:  

![Gobbo HUD example Green Fists](/_img/mechanics/HUD/HUDGobbo.png)

![Orc HUD example Fists](/_img/mechanics/HUD/HUDOrcSlave.png)

And since we add Madness as a seperate attribute in the sense of "negative Willpower", as described above, we also have new dedicated Madness Symbols:  

![New Madness Symbols](/_img/mechanics/HUD/HUDMad2.png)


#### Enhanced Bar HUD

The bar HUD will follow the brutalist style and function from ~v0.8-0.9.  
But just as the Symbol HUD the bars will be smaller for characters with smaller values and larger for characters with larger values, not being stretched to a fixed width like in the release version. Instead of adjusting the bars to the background texture, we will adjust the background texture to the bars. This will not only provide additional information to the player, the HUD will also cover less of the screen.  

![Shorter Bars](/_img/mechanics/HUD/bar-hud-new.png)


### Beyond the HUD

We will also go beyond the HUD completely (apart from the inventory) by radical attribute visualisation that makes both the Icon and the Bar HUD optional.  

In this regard, allow me this pathetic metaphor: Just as "that government is best which governs the least" (Thoreau), because it creates conditions of self-regulating autonomy under which its intervention isn't needed anymore as the people are able to govern themselves; that HUD (heads-up display) is best which has to be displayed the least, because the developers created conditions of self-explanatory gameplay mechanics by which its representation isn't needed anymore as the players are able to *play it* themselves. A metaphor for Gothics minimalist interface design.  

And just as I am not demanding for the government to just be taken down, but for it to remain fully functional as necessary while realising it as its primary function to make itself unnecessary (at which all governments fail, thereby undermining their own legitimacy); and to the same degree as the government is needed, to this very degree it exposes the lack of autonomy established in society which it needs to govern less (and for us to be more free) - In the same way we aren't demanding to eliminate the HUD, but we want that it is not *needed*, because to the same degree as the HUD is needed, to this very degree it exposes a lack of visualisation established in the gameplay which we need for less abstraction (and for us to play more immersed).  

This said, we do not strive to get rid of the HUD altogether, but we want it to be optional and for the game to be fully functional (= playeable) without it. 

The HP reduction will be visualised by enhancing the idea experimented with in v0.64b as described in ["Overcoming the Hud"](#overcoming-the-hud). Before seeking refuge in pfx effects we have to consider equivalent solutions of animations for the discharge and exhaustion of Mana and Psi. Their visualisation has to be strongly correlated with how these attributes function.  

Just as there is an overlay when the character is injured - has less than X HP -, there will be an overlay when the character has less than X Psi- or Mana points. When the psionic reaches the end of his Psi treshold, the demonic force begins to pressure him and he gets headaches; at this point he will walk around with his hand on his head, turning and shaking his head while standing, not being able to run, signifying to the player that his character is on the edge and madness is nigh. This will be accompanied by a progressively increasing droning sound effect and a mild visual effect.  

<p class="subtext">Related fun fact: Mike wrote in his notes that psionics should only be able to cast psi spells as long as they don't wear a helmet.</p>

While the animation overlay of the psionic visualises how his magic is mainly associated with his mental power by laying the focus on his head, the magic of the Arcane Mages is different, alchemical and associated with the Mana in his bloodstream (more on that in the "Alchemical Magic" document). Hence when he is close to the edge of Madness his overlay has to show how the lack of Mana (that serves as a physical protection from the demonic forces just as the Psi serves as a psychical protection) is affecting his whole body similar to an addict on withdrawal. He will be shown bent over, scratching his arm or looking at his hand. 


#### Possession

When X points of Madness are reached, a character is possessed. When he reaches this state his eyes turn red (texture change) as described in Alex Story (and as shown in form of the fanatics in the release version of the game).  
Lower level characters will flee when perceiving someone in the possessed state, unless they are possessed themselves. Characters on the same or a higher level (when neutral or angry) will draw their weapon / magic and shout at him to go away. Friends will immediately speak to him and try to help him with drugs if they have any.  

But more than that: When the player character is possessed, the player will not be completely in control anymore. His character will do things against the will of the player for the player to experience being unwillingly controlled. He is in a fight between the influences of the demonic force and of what he wants to do himself. The force drives him towards violence and blood; he has to struggle against himself and regain sanity before it is too late.  


### Summary

In the process of structuring these mixed attributes and my attempts to organise them for the character screen, we asked the question what attributes usually stand for in a roleplaying game.  

> An **attribute** is a piece of data (a statistic) that describes to what extent a fictional character in a role-playing game possesses a specific natural, in-born characteristic common to all characters in the game.  

According to this definition the arts cannot be considered as attributes, since they are no characteristics common to all characters nor are they natural or inborn. The ones that would fit that description are only the following ones, which I structure in a simple scheme:  

* `ATR_Strength` (+ `ATR_Hitpoints`) = Physical Power
* `ATR_Constitution` (+ `ATR_Endurance` = Physical Condition)
* `ATR_Will` (+ `ATR_Madness` = Mental Power & Condition)

<!--
```
`ATR_CONSTITUTION` = Physical Condition
`ATR_STRENGTH`     = Physical Strength
`ATR_DEXTERITY`    = Physical Control

`ATR_MADNESS`      = Mental Condition
`ATR_WILL`         = Mental Strength
`ATR_PSI`          = Mental Control
```
-->

<!--Psi fits into the scheme as mental control; but as almost no one has control over his mind it is not actually to be seen as a general attribute (but as a potential one); everyone has some degree of control over his body, but regarding the mind, most characters in the game (like in reality) are not in control and experience their mind primarily as a sheer force of wanting or mentally resisting, they can't stop the stream of thought (and this will play a role again in the second act of Phoenix, when the sect is destroyed, but the "psionic" art lives on).-->    

Thus, the rest is either a mere representation of these for the player in form of the HUD or it has to belong to the specific experience in the Arts or "Gifts". And while the four arts described above are class-specific, we have added additional class-crossing ones, where Logx is to credit for the idea of *Metallurgy* and *Huntsmanship* here:  

```
Class specific:       Class crossing:

* EXP_WEAPONRY        * EXP_ALCHEMY
* EXP_THIEVERY        * EXP_METALLURGY
* EXP_ARCANERY        * EXP_MARKSMANSHIP
* EXP_PSIONICS        * EXP_HUNTSMANSHIP
                      * EXP_PHILOLOGY
                      * EXP_ARMORY
```

*Alchemy* is class-crossing in that it is dealt with by both Mages and Psionics; in the same way as *Archery* or *Marksmanship* and *Huntsmanship* (part of which is all kinds of knowledge about monsters) are relevant for both warriors and thieves. *Metallurgy* does not only matter for forging swords, but begins with common knowledge about ore and ends in refined arts such as runemaking (which is *arcane*). This way, some arts and the experience gained in them has synergistic effects on others.

---

Therefore, there are 7 values (3 primary attributes - where Will and Madness are counted as one, since Madness does only appear in absence or loss of Will - and 4 main Arts or forms of experience) that are displayed in the character sheet by descriptive text; they are referred to inside the game by clear texts or speech and connect the game's mechanics with its lore. Among the arts only those are displayed in the character sheet that the character in question has actual experience in:  

* `ATR_Constitution` (scaled by Level)
* `ATR_Strength` (scaled by Weaponry)
* `ATR_Will` / `ATR_Madness`   

* `EXP_*`  

The following attributes are secondary or "status attributes". The first three are not mentioned or referred to in the game, they serve primatily internal purposes in the game logic, they are only represented in the HUD and are scaled by primary attributes or arts. Mana and Psi are referred to inside of the game as "magic energy" or "psi energy" respectively:  

* `ATR_Hitpoints` (scaled by Strength)
* `ATR_Endurance` (scaled by Constitution)
* `ATR_Dexterity` (scaled by Thievery)
* `ATR_Mana` (scaled by Arcanery)
* `ATR_Psi` (scaled by Psionics)

There are indicators/counters of the character's health regarding nutrition, fatigue, intoxication and magical radiation exposure, that are displayed in the character screen and affect the HUD (they change the coloration of the health bar inside the Bar HUD and add additional symbols in the Symbol HUD): 

* `ATR_Nutrition`  
* `ATR_Fatigue`  
* `ATR_Intoxication`  
* `ATR_Radiation`  

The following attributes and related constants are not referred to in the game world and are solely displayed in the form of the HUD or serve pure internal functions. Apart from `EXP` there is another new constant added for regeneration (`REG`):

* `REG_*` (Regeneration)
* `DMG_*` (Damage) 
* `PROT_*` (Protection)
* `RES_*` (Resistance)

There are the following categories of regeneration:

* `REG_Life` (Hitpoints Recharge)
* `REG_Energy` (Endurance Recharge)
* `REG_Sanity` (Madness Reduction)

* `REG_Mana` (Mana Regeneration for Mages)
* `REG_Psi` (Psi Regeneration for Psionics)
* `REG_Special` (Special Attacks for Warriors)
* `REG_Focus` (Special Focus for Thieves)


And that's it. This is our solution, making for a coherent system, that is both simple and complex.  



<div class="authorship">
    <img src="/_img/authors/flosha-sm.png" alt="Flosha">
    <p>
        <strong>Author:</strong> Flosha<br>  
        <em>Creative Director</em><br>  
        <br>
        <strong>Written:</strong> 30.12.18 - 27.12.20<br>  
        <strong>Rewritten:</strong> 03.11.22 - 04.12.22<br>  
        <strong>Changed:</strong> 27.05.2023
    </p>
</div>
