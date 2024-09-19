# Decision Trees

*Flosha, 19.10.2024*

Structured by relation tables  
Every relation = one decision  
      (by roleplaying)


```
CH1:  Choose Camp/Class > Guild Decision
CH2+: Camp/Class/Guild-bounded Story Decisions
```


## CH1

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

## CH2



Escape Plans:
```
VLK:Survive
MAF:StatusQuo
PSI:Massprayer
NC/FC:Destroy[?]
KDF:Research

CH2: SupportPSI </> SupportCircles



ResearchBarrier </> DestroyBarrier
```

CH2:
OC: ...
PSI

CH3:

OC:  Support KDF <> EBR
PSI: Support Angar <> Kalom
NC:  Support Lares <> Lee
FC:  ...





