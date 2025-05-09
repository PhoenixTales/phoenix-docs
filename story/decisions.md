# Decisions

*Flosha, 19.10.2024*







*Decision Trees* structured by relation tables. Every relation equals one decision by roleplaying.  


```
CH1:  Choose Camp/Class > Guild Decision
CH2+: Camp/Class/Guild-bounded Story Decisions
```


## CH1 - Orientation

```
CH1 >
  Camp > Guild
     || Class > Guild
         > CH2
```


### Camp > Guild

JoinCamp:
```
OC <> FC  |  FC <> NC  |  NC <> OC
PSI <> NC |  OC <> PSI | PSI <> FC

     OC </> FC </> NC </> PSI
```

Mission Perspectives:
```
OC <> FC      FC <> OC
OC <> NC      FC <> NC
OC <> PSI     FC <> PSI

NC <> OC      PSI <> OC
NC <> FC      PSI <> NC
NC <> PSI     PSI <> FC 
```

OC > JoinGuild:
```
STT <> GRD
GRD <> KDF
KDF <> STT
```

FC > JoinGuild:
```
NONE - freedom; resulting
in a thief/warrior hybrid
```

NC > JoinGuild:
```
ORG <> SLD
SLS <> KDW
KDW <> ORG
```

PSI > JoinGuild:
```
NOV <> TPL
```


### Class > Guild

ChooseClass:
```
FIGHTER <> THIEF
THIEF <> MAGE
MAGE <> FIGHTER
PSION <> MAGE
FIGHTER <> PSION
PSION <> THIEF
```

Class > JoinGuild:
```
FIGHTER: GRD </> SLD </> TPL
THIEF:   STT </> ORG </> FLL
MAGE:    KDF </> KDW
PSIONIC: -
```

---


### Character Forming Decisions / Opinions / Positions

In the original game, the player was able to decide for a camp, he was able to decide for a guild and so on. But he was *never* really able to develop his character in any way that would suggest an actual preference or loyalty to a camp, guild or faction. Based on the original game, the player could *never* really know, nor could he himself decide, whether or not his character actually liked the guild he played for, if he actually stood behind the stuff they did and they believed in. The player, while playing a role, was not really able to shape this role in any way other than the guild decision which hadn't much more consequence than wearing a different armour. In this way, the roleplaying was very poor.

What we want to do instead is to give the player several actual decisions to make, by which he can shape his character to his liking to some degree. For instance: We want that a player can both join a camp in a merely opportunistic kind of way, or by actual preference and conviction. This difference will then have to have consequences later on for additional decisions and will result in different dialogue options. For instance: The player may defend his guild, his faction or his camp in disputes with others; or he may rather be indifferent towards it. The point is that a few early decisions by which the player is *expressing* his preferences (upon learning a bit about the different factions), has to open up future dialogue options which should be different compared to those he would receive if expressing a different preference (or indifference) earlier in the game. 

It is only in this way that we can give the player an actually unique direction to develop his character into and a connection between him and the character; the player *has* specific preferences, he *has* or often would like to have some actual loyalty to a guild, but he cannot express it in the game and cannot act accordingly. 

We want that in the end, when asked about how he played his character, a player can tell us not only: "I joined the Organisation and completed the game as a Thief", but that he can tell us something like: "I joined the Organisation and played very loyal to Lares, having some conflicts with Lee. I hated the Old Camp and played accordingly, choosing to participate in the robberies of the Convoys; I didn't think that the ritual of the Brotherhood would be any good and did *not* help them; my character believed in the Escape Plan of the Mages until its failure, and even after talking to Xardas I decided to inform my leaders, the Watermages, of what I had learned, instead of working behind their back."  

You can see by the example above, that there may be another player, who also joined the Organisation, who may describe his story in a very different way. He may have joined the Organisation for other reasons. He may have a different opinion about the plan of the Sect or the plan of the Watermages or the loyalty to Lares and Lee and so forth. 


---




## CH2 - Ritual Involvement

Main: `Support Sect </> Circles (KDF </> KDW)`

InterestsCH2:
```
VLK:Survive
MAF:StatusQuo
PSI:Massprayer
NC/FC:Ore (Foci?)
KDF:Research
```

## CH3 - Internal Conflicts

Camp-bounded Decisions
```
OC:  Support KDF <> EBR
PSI: Support Angar <> Kalom
NC:  Support Lares <> Lee
FC:  ?
```

Class-bounded Decisions:
...

Guild-bounded Decisions:
...


## CH4 - Faction War

Main: `FindTemple`

```
OC:  Loyal to the Barons or not
NC:  Orc Alliance or not?
PSI: OC Alliance <> NC Alliance
FC:  Reconquer/Rescue
```


## CH5 - OrcAssault

Main: `AccessTemple`

Truce:
```
OC:  Stopping the Revolt
NC:  Truce with OC 
PSI: Influencing the Revolt / Temple
FC:  Influencing the Revolt
```


## CH6 - Nemesis

Main: `BanSleeper`
