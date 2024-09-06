# World Design

<img class="world" src="/_img/world/overworld.jpg">

In this part of the documentation we are dealing with the design of the game world, starting with its level structure, the evolution of the world map and layout (the gothic kingdom as a whole is dealt with in the /lore). We proceed with the landscape of the colony and the explorable sections of the outside world and the climate as well as the vegetation inside and outside of the barrier, then continue with the monsters inhabitating the world and how they evolved under the influence of the barrier. 

In the main part we will analyse the evolution of all the locations; the camps and the city in particular - including their layout, artstyle, architecture, their pattern or possibilities of exploration and their historic background. This section is divided into overworld, underworld, outside world and demon world. The locations within the colony are first dealt with in relation to our first act, then in "Colony Revisited" in relation to our second act (after the fall of the barrier). 

Finally we will deal with the different factions and guilds as they live in and live up the game world and their role in shaping the same. Including general considerations of their role-specific A-life in the simulated world as well as dealing with their visuals (body, costumes/attire, equipment). 
 
At the end of the analyses of each of these topics within the before mentioned categories (landscape, vegetation, monsters, locations, guilds and character visuals), we will summarise our findings, before presenting our solution for Phoenix. As in the other sections of the documentation, "Alpha Research" and Phoenix Gamedesign are thereby clearly discernible.

<!-- In the Act II section we will deal with what the Sequel team wanted to do with the colony in their project, with the limitations they were facing and also, in parts, with what went wrong with the level design of the official sucessor - arising in a critique against the Sequel, while falling far behind it in its artdirection and loosing any gothic themes and aesthetics - before dealing with our own world design for act 2. We will then elaborate how we approach the design of the outside world (Khorinis surroundings); but the majority of this section will cover the design of the *City*. -->

<!--In this context we will also have to deal with the NPCs and their initial placement ("start routine") in the world (the "setup" that the player will be confronted with).--> 

<!--
Finally we will deal with the placement of objects (non-takeable, static objects, moveable or useable objects as well as takeable objects, items).

Perhaps: Rather deal with items in a section at the bottom of every single location?
Or deal with items in the plot, when dealing with the exploration of specific locations!!! -->

<!-- Costume Design may be a subcategory within the guild docs -->

--- 

**Content:**

1. World Map & Layout
	1. [Level Structure](/story/level-structure)
	2. [Evolution of the Map](/story/map-evolution)
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
            1. Cliff & Exchange Place
            2. Abandoned Mine Outside
            3. Old Pass & Troll Canyon
            4. Hidden Bandits Hideout
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
            1. Hermit's Valley
            2. Psi Camp
            3. FogTower 
            4. Stone Circle 
            5. Lighttower
            6. Beach & SmugglersBay
            7. Monastery Ruins
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
            2. Old Mine
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
    3. Outside World
        1. Abandoned Factory
        2. Old Fortress
        3. Franks Castle
        4. Half-Orc Camp
        5. City Design
            1. Older City 
                1. Castle
                2. Monastery
                3. Orphanage
                4. Manufactures
                5. Manors
            2. Newer City
                1. Ore Factory
                    1. Cathedral
                2. Manufactures
                3. Ghost District
                4. Varantian Quarters
                5. Slavemarket
            3. Slums
            4. Canalisation
            5. Catacombs
    4. Demonworld
        1. Demonic Overlays
        2. Demon Tunnels
6. [Faction Design](/story/factions/factions)
    1. [Guilds](/story/factions/guilds-descriptions)
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
                * Mercenaries
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
                * Royal Guard
                * Royal Army
            5. Law
                * Royal Judges
                * Inquisition
                * Black Guard
                * Royal Shadows
            6. Outlaws
                * Anti-Royal KdW
                * Demonhunters
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
