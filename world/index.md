# World Design

<img class="world" src="/_img/world/overworld.png">

```
Author: Flosha / Written: 05.09.2024 / Update: 06.09.2024
```
{: .info }

In this part of the documentation we are dealing with the design of the game world, starting with its level structure, the evolution of the world map and layout (the Gothic Kingdom as a whole is dealt with in the /lore). We proceed with the landscape of the colony and the explorable sections of the outside world and the climate as well as the vegetation inside and outside of the barrier, then continue with the monsters inhabitating the world and how they evolved under the influence of the barrier. 

In the main part we will analyse the evolution of all the locations; the camps and the city in particular - including their layout, artstyle, architecture, their pattern or possibilities of exploration and their historic background. This section is divided into overworld, underworld, outside world and demon world. The locations within the colony are first dealt with in relation to our first act, then in "Colony Revisited" in relation to our second act (after the fall of the barrier). 

Finally we will deal with the different factions and guilds as they live in and live up the game world and their role in shaping the same. Including general considerations of their role-specific A-life in the simulated world as well as dealing with their visuals (body, costumes/attire, equipment). 
 
At the end of the analyses of each of these topics within the before mentioned categories (landscape, vegetation, monsters, locations, guilds and character visuals), we will summarise our findings, before presenting our solution for Phoenix. As in the other sections of the documentation, "Alpha Research" and Phoenix Gamedesign are thereby clearly discernible.

<!-- In the Act II section we will deal with what the Sequel team wanted to do with the colony in their project, with the limitations they were facing and also, in parts, with what went wrong with the level design of the official successor - arising in a critique against the Sequel, while falling far behind it in its artdirection and loosing any gothic themes and aesthetics - before dealing with our own world design for Act II. We will then elaborate how we approach the design of the outside world (Khorinis surroundings); but the majority of this section will cover the design of the *City*. -->

<!--In this context we will also have to deal with the NPCs and their initial placement ("start routine") in the world (the "setup" that the player will be confronted with).--> 

<!--
Finally we will deal with the placement of objects (non-takeable, static objects, moveable or useable objects as well as takeable objects, items).

Perhaps: Rather deal with items in a section at the bottom of every single location?
Or deal with items in the plot, when dealing with the exploration of specific locations!!! -->

<!-- Costume Design may be a subcategory within the guild docs -->

--- 

**Content:**

1. World Map & Layout
	1. [Level Structure](/world/level-structure)
	2. [Evolution of the Map](/world/map-evolution)
	3. Layout of the World
2. Landscape & Climate
    1. The Valley of Mines
	2. Falls, Lakes, Rivers, Springs
	3. Islands
	4. The Swamp of Lost Souls
    5. Sea & Coastline 
3. Flora / Vegetation
    1. Plants & Mushrooms
    2. Forests 
        1. Northern Forest
        2. Western Forest
        3. Eastern Forest
        4. Swamp Forest
        5. Demon Forest
        6. Outside Forest
        7. Mystic Forests (Act 2)
4. Fauna / Monster Design
    1. Mammals
        1. Molerats
        2. Wolves
        3. Bloodhounds
        4. Orcdogs
        5. Harpies
        6. Shadowbeast
        7. Trolls
            * Cavetrolls
            * Mountaintrolls
    2. Reptiles
        1. Scavenger
        2. Gobbos
        3. Lurkers
        4. Snappers
        5. Swampsharks
        6. Warans
        7. Vultures
    3. Insects
        1. Meatbugs
        2. Bloodflies
        3. Minecrawlers 
        4. Minesprayer
        5. Mushgroomer
    4. Undead
    5. Demons
5. Locations
    1. Overworld
        1. Middle of the Colony
            1. Hangman's Tree
            2. Old Camp / Castle
            3. Western Plateau
            4. Eastern Grasslands
        2. Northern Environment
            1. [Northeast](/world/northeast) 
                * Northern Forest
                * Northern Lake(s)
                * Cliff of the Damned 
                * Exchange Place
                * Abandoned Mine Outside
                * Hidden Bandits Hideout
                * Old Temple Ruins
            2. Northwest
                * Troll Canyon
                * Old Pass to the North
                * Old Pass to the West
        3. Western Environment 
            1. New Camp
            2. Rock Cemetary & Tombs
            3. Free Camp
            4. OrcCaves Entrance
        4. Southern Environment
            1. Old Fort
            2. Old Mine Outside
            3. Demontower & Cliffs
            4. Mountain Fortress
        5. Eastern Environment
            1. Eastern Shore
                * Lighttower
                * Beach & Smugglers Bay
                * Stone Circle 
            2. The Swamp
                * FogTower 
                * Hermit's Valley
                * Psi Camp
        6. Colony Revisited (Act 2)
            1. Refugee Camp (Mst)
            2. Infected Mine
            3. Old Fortress (Tym)
            4. Abandoned Camp 
            5. Demon Camp (Dmc)
            6. Surface Destruction
            7. Mystic Forests 
        7. Passes and Borders
    2. Underworld
        1. Mines
            1. Abandoned Mine
            2. Old / Lost Mine
            3. Free Mine
            4. Fog Mine
        2. Monster Lairs 
            1. Gobbo Caves
            2. Troll Hoards
            3. Bld/Crw Nests
            4. Lurker Nests
            5. Shadow Caves
            6. Sprayerlair
            7. Dragon Hoard
        3. Natural Caves
        4. OrcCaves
            1. OrcCity
            2. OrcGraveyard
        5. AncientTemple
            1. Level 1
            2. Level 2
            3. Level 3
            4. The Abyss
            5. The Citadell
    3. Outside World
        1. Abandoned Factory
        2. Old Fortress
        3. Moor / Franks Castle 
        4. Half-Orc Camp
        5. City Design
            1. Older City
                1. Castle
                    1. Fire Fortress
                    2. The Asylum
                2. Upper Streets
                    1. Monastery
                    2. Orphanage
                    3. Manors
                    4. Warehouse
                3. Lower Streets
                    1. Gutter
                    2. Canal
                    3. Manufactures
            2. Newer City
                1. Ore Factory
                    1. Cathedral
                2. Manufactures
                3. Ghost District
                4. Varantian District
                    1. Workers Quarters
                    2. The Suq
                        1. Trading Centre
                5. Slavemarket
                    1. Panopticon
            3. Slums
            4. Canalisation
            5. Catacombs
    4. Demonworld
        1. Demonic Overlays
        2. Demon Tunnels
6. [Faction Design](/world/factions/)
    1. [Guilds](/world/factions/guilds/guilds-descriptions)
        1. Orpheus
            1. Folk
                * Miners
                * Workers
                * Merchants
                * Beggars
                * Peasants
            2. Mafia
                * Orebarons
                * Thugs/Guard
                * Snitches/Shadows
            3. Mages 
                * Circle of Fire
                * Circle of Water
            4. Anti-Royal 
                * [Gladiators/Mercenaries](/world/factions/guilds/demonhunters)
                * Organisation
                * Rogues
            5. Heretics 
                * Psionics
                * Demon Summoner
            6. Revolt 
                * Scraper's Union
                * Silence
	    7. Bloodearth Clan
        2. Nemesis
            1. Folk
                * Workers
                * Peasants
                * Merchants
                * Healers
                * Beggars
                * Auxiliaries
            2. Magnates
                * Orebarons
                * Drugbarons
                * Varantian Tradersguild
            3. Clergy
                * Royal Mages
                * Circle of Fire
                * Circle of Water
                * Anti-Royal Monks
            4. Royals
                * Royal Court
                * Paladins
                * [Royal Guard](/world/factions/guilds/royal-guard.md)
                * Royal Army
            5. Law
                * Royal Judges
                * [Inquisition](/world/factions/guilds/inquisition)
                * [Black Guard](/world/factions/guilds/black-guard)
                * Royal Shadows
            6. Outlaws
                * Anti-Royal KdW
                * [Demonhunters](/world/factions/guilds/demonhunters)
                * Bandits
            7. Revolt
                * Scrapers Union
                * Silence
                * Slave Rebellion
            8. Heretics
                * Mystics
                * Demonsect
                * Amazons
                * Demon Summoners
            9. Pariahs
                * Possessed
                * Half-Orcs
            10. Clans
                * Bloodearth
                * Dreamfire


<style>

    main {
        background: url("/_img/bg/world2.jpg");
        background-position: top right;
        background-size: 75%;
        background-repeat: no-repeat;
        width: 100%;
    }

    .world {
        display: block;
        image-rendering: pixelated;
        max-height: 550px;
        max-width: 100%;
        margin: 0 auto;
    }
        main .article h1 {
            font-size: 22px;
        }

</style>
