# Decision Trees

*Flosha, 19.10.2024*

Structured by relation tables  
Every relation = one decision  
      (by roleplaying)


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

## CH2 - FocusHunt

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
FC:  ...
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
~~FC~~
```


## CH5 - OrcAssault

Main: `AccessTemple`

Truce:
```
OC:
NC:   
PSI:
~~FC~~
```


## CH6 - Nemesis

Main: `BanSleeper`
