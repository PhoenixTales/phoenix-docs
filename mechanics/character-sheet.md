# Phoenix Character Sheet

*flosha, 08.08.2026*

Info: A rough WIP mockup of the character sheet; first in text form before applying any design.


## General guidelines

We use the latest known top layout as presented in v0.94k, but we (1) do not display the spells, we will (2) not display talents/skills and we'll also (2) not display active/old missions on the character screen. Instead...
  * We will display spells in a dedicated spell book of the mage; which may as well be a subcategory of his log screen with an extra design/texture, because the amount of spells would be just too much and it wouldn't serve warriors/thieves anything to have a display of spells in there. 
  * We will list talents in the log screen as well, where there will be a "talent" (Skills/"Fertigkeiten") category, in which all learned talents will be listed, ordered into the different arts that they belong to, because there are way too many weapon and thief skills most of all, and some arcane and psi related skills as well, that will take up too much space and most won't be relevant for the character due to his class. 
  * Missions we will list as usual in the log screen too, as established by the later versions of the game.
  * Eventually though, the character screen as well may become a subcategory (the main page) of the log screen; in this way, we follow the alpha vision insofar, as that both will be combined again (but separate in the categories selectable on the left). The log screen is eventually to be designed as follows:

```
+ ----------------------------+
|  Character |                |
|  Skills    |                |
|  Spells    |    Content     |
|  Missions  |                |
|  Infos     |                |
+ ----------------------------+
```

But for now, and at this place, we only want to consider the character sheet in isolation. Whether a separate screen or included in the log screen, we plan to display the following information in the character sheet: 
1. General infos consisting of:
   * Name/Nickname (in case of the player character it is the nickname that is given to him by NPCs in the game world, the one that the other characters adapt, which changes in course of the story).
   * Guild (in earlier documents also called "Bande")
   * Rank within his guild (which roughly corresponds to the Level (there will be 6 or 7 total levels), while the Level roughly corresponds to the Chapter he is in, which is one of six). 
2. Primary Attributes in descriptive clear text form
3. Secondary/Status Attributes.

**Reservation:** Secondary Attributes may be displayed in icon form as within the Icon HUD, maybe in form of numbers. We will for now plan to present it in the character sheet in some form, for completeness sake and structure. But in the end our goal may be that they are not displayed in the Character Sheet at all, because the HUD or the Visualisation is meant to suffice: 
* When using the Icon HUD you know that you are hungry and how much, you know how much Mana you have or not and how much you can currently have; you know all this info already and don't need it again in the character sheet, which would just be a duplicate of that information that you already have access to in more direct ways. For example, there is no need whatsoever to display the required strength value of a sword, if we include a function in the IconHUD that immediately shows us how much strength would be necessary in order to use it efficiently (e.g. by small slowly blinking fist icons that are lacking; the player then immediately sees: "Okay, to use this weapon or armor well, I lack e.g. 2 strength points").  
* In case of the Bar HUD we try to provide the same information in an unobtrusive way. How has yet to be clarified. If it is supposed to show the very same amount of information that the Icon HUD can provide, it will only work when, at least while opening the inventory etc., additional bars are displayed e.g. for strength; if so the bar could show you how much more it has to rise in order for a weapon to be used efficiently, for instance. But all of this may be much less complicated than it seems depending on the balancing in the end: From the sources we know that just as with armors, where there are only three main variants (light, medium, heavy), weapons too would have been divided like this. If you can effectively fight with one medium weapon, you can do so with all medium weapons. Thus you only have to know, whether or not you have a moderate amount of strength sufficient for the weapons of that category, the PC can say something (like the usual sentence "This is too heavy for me", a dealer may tell you whether you are strong enough for this or that sword and so on. 
* We also want to enable gameplay without any HUD and so we try to provide all this information immersively (via animations, verbal cues, sound effects and pfx effects). 

For a neat, consistent order, we also could somehow summarise the above information as such (German):
* Allgemeine Charakterinfos: Name, Gilde, Rang/Level
* Konstitution -> Ausdauer & Regeneration -> Körperliche Verfassung 
* Körperliche Kraft -> Körperliche Künste + Statuswerte 
* Geistige Kraft (Wille) -> Geistige Künste + Statuswerte 
* Geistige Verfassung (Wahnsinn/Sanity) -> Geistige Gesundheitswerte 


## Text-based Mockup

Below I provide two text-based layout concepts, at the example of Y'Berion. In both cases, the information would easily fit into the character screen as well as into the right side of the log screen. As secondary professions he knows minor alchemy and orcish (language) basics; no other art is displayed when an NPC has not learned any other additional art (e.g. huntsmanship etc.). Also, in case that status values are displayed (V1), only those status values are displayed that are relevant to the character's class. 
* Guildless characters, thieves or warriors: No mana, no psi.
* Mages: Only Mana, no psi.
* Psionics: Only psi, no mana.


**Layout Concept V1**  
*with status attributes displayed on the right side, with no relation to the left*   

```
+--------------------------------------------------------------------------+
| Name: Y'Berion         Gilde: Gurus      Rang:  Der Erleuchtete (lvl: 7) |  
|--------------------------------------------------------------------------|
|            ATTRIBUTE            |              STATUSWERTE               |  
|---------------------------------|----------------------------------------|
| Konstitution      anfällig (32) |        Lebensenergie               10  |
| Kraft              schwach (30) |        Stärke                       5  |
| Wille               eisern (85) |        Geschick                     5  |
|                                 |        Ausdauer                     ?  |
| Waffenkunst       wehrhaft (25) |        Psi                         30  |
| Diebeskunst     unbeholfen (10) |                                        |
| Arkane Gabe          keine  (0) |        Hunger                       x  |
| Psionik         erleuchtet (80) |        Durst                        x  |
|                                 |        Müdigkeit                    x  |
| Alchemie              XYZ  (20) |        Vergiftung                   x  |
| Sprachkunst           XYZ  (30) |        Wahnsinn                     x  |
+--------------------------------------------------------------------------+
```

**Layout Concept V2**  
*clean, without status attributes  
(based on the premise that they are  
displayed sufficiently in the HUD)*  

```
+---------------------------------+
| Name: Y'Berion                  |
| Gilde: Gurus                    |
| Rang:  Der Erleuchtete (lvl: 7) |  
|---------------------------------|
|           ATTRIBUTE             |
|---------------------------------|
| Konstitution      anfällig (32) |
| Kraft              schwach (30) |
| Wille               eisern (85) |
|                                 |
| Waffenkunst       wehrhaft (25) |
| Diebeskunst     unbeholfen (10) |
| Arkane Gabe          keine  (0) |
| Psionik         erleuchtet (80) |
|                                 |
| Alchemie              XYZ  (20) |
| Sprachkunst           XYZ  (30) |
+---------------------------------+
```

**Layout Concept V3**  
*with status attributes displayed on the right side,*  
*but **with** a relation to the left; at least partially:*  
*Kraft scales Leben & Stärke, Konstitution scales Ausdauer  
and Wille scales Psi and protects from Wahnsinn; but sadly  
Geschick doesn't fit here and the four health values would  
also fit somehow to both Kraft & Konstitution, affecting it.  
But no idea yet if that can somehow be visualised nicely  
and if it has to; since it also works fine as above.*  

```
+--------------------------------------------------------------------------+
| Name: Y'Berion         Gilde: Gurus      Rang:  Der Erleuchtete (lvl: 7) |  
|--------------------------------------------------------------------------|
|            ATTRIBUTE            |              STATUSWERTE               |  
|---------------------------------|----------------------------------------|
| Kraft              schwach (30) |   Leben       10      Stärke        5  |
| Konstitution      anfällig (32) |   Ausdauer     ?      Geschick      5  |
| Wille               eisern (85) |   Psi         30      Wahnsinn      5  |
|                                 |                                        |
| Waffenkunst       wehrhaft (25) |    Hunger      x      Durst         x  |
| Diebeskunst     unbeholfen (10) |    Müdigkeit   x      Vergiftung    x  |
| Arkane Gabe          keine  (0) |                                        |
| Psionik         erleuchtet (80) |                                        |
|                                 |                                        |
| Alchemie              XYZ  (20) |                                        |
| Sprachkunst           XYZ  (30) |                                        |
+--------------------------------------------------------------------------+
```













