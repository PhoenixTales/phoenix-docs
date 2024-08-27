# Factions

**Author:** *Flosha*  
**Created:** 02.11.2022   
**Changed:** 27.08.2024  
**Status:** <span class="changed">work in progress</span>  

By factions we mean groups of guilds within and across camps; or in short: Factions are cross-camp groups of guilds. I introduced them to simplify the complex "guild attitudes" by working with _layers of relations_ from general to specific (see [Relations]()). It is a system that enables us to take both Act 1 and Act 2 factions/guilds into account. 

The factions serve primarily the internal purpose of structuring guilds by e.g. the common dramaturgical functions (DraFu) they serve, but they also correspond to groups of people as mentioned within the game.
Currently we distinguish between the following factions:

* Folk
* Magnates
* Priests
* Royals
* Law 
* Outlaws
* Revolt
* Heretics
* Slaves
* Exiles/Pariahs


## Internal Shortcuts

[Vlk] Volk (Folk)  
[Mgt] Magnaten (Magnates)  
[Prs] Priester (Priests)  
[Kng] Königliche (Royals)  
[Rch] Richter (Judges/Law)   
[Vgf] Vogelfreie (Outlaws)  
[Fre] Freie (Freedom/Revolt)  
[Ktz] Ketzer (Heretics)  
[Slv] Sklaven (Slaves)  
[Exi] Verstoßene (Exiles)  


## Guilds per Faction

* Folk (Diggers, Workers, Beggars, Aux, ...)
* Magnates (Mafia, Varantian Trader's Guild, ...)
* Priests (Firemages, Watermages, Monks)
* Royals (Royal Family, Paladins, Royal Guard)
* Law (Magistrates, Inquisitors, Black Guard)
* Outlaws (Gladiators, Orgas, Bandits, ...)
* Revolt (Silence, Scraper's Union, Rangers)
* Heretics (Psionics, DMC, MYS, AMZ, DMB, ...)
* Slaves (Peasants, Women, Orcs, Demons, ...)
* Exiles (Possessed, Halforcs, ...)


### Subfactions

* Psionics: Novices, Templars, Gurus 
* Mafia: Orebarons, Baron's Mercs (Guard), Shadows
* ... 


#### Examples

Past LastPrayer Psi is split into Moderates & Fanatics (Mad).  
In Nemesis, the remnants of Psi form the Mystics (Psi → Mys).
While the outlasting Fanatics form the DemonCult (Mad → Dmc).
They are all considered as Heretics by Law, Royals & Priests.


## Factions per Camp

### Act I
* Old Camp: Folk, Mafia, Priests (KDF), Slaves
* Free Camp: Revolt (Silence, Scrapers, Rangers)
* New Camp: Outlaws, Folk, Priests (KDW), Slaves
* Psi Camp: Heretics (Psionics), Slaves


## Implementation

Constant: FAC_* [e.g. FAC_VLK] 

```
    
    VLK     // Folk       // BDL, ARB, BTL, AUX
    MGT     // Magnates   // MAF, VAG
      MAF   // Mafia      // EBR, GRD, STT
    PRS     // Priests    // KDF, KDW, KDL
    KNG     // Royals     // KNG, PAL, KGD
    RCH     // Law        // INQ, SGD
    VGF     // Outlaws    // SLD, KDW, ORG, BAU, BDT
    REV     // Revolt     // MST, SFB, FLL
    KTZ     // Heretics   // PSI, AMZ, DMC, DMB
      PSI   // Psionics   // NOV, TPL, GUR
    SLV     // Slaves     // BAU, BAB, ORC, DEM
    PAR     // Pariahs    // POS, HLF

```