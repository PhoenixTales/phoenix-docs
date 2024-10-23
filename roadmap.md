# Phoenix Roadmap

```
Last update: 14.09.2024
```
{: .info }

This page serves the purpose of informing you about the progress of Phoenix: What has been done so far, what is currently done, what still has to be done, what we are currently capable of doing and where progress depends on additional help (also see [/contrib](https://phoenixthegame.com/contrib)).

TLDR: Right now Flosha is working alone on the documentation and on the Phoenix build, focused on world modeling. Auronen is working on tools in the background, that are both instrumental for our project and of help for the community at large. Avallach is in the process of fixing our Gothic Archive and improving its performance (it can currently not be updated due to storage problems). <!-- He is doing some supportive research in regard to inspirations of Gothic, but is not actively involved in development at the moment. -->

There is no one else currently at work. A few long-term contributors support us occasionally. 

<!-- TOC_PLACEHOLDER -->

## Short-term Goal

We want to release a first tech demo focused on Item Handling, our Inventory System, our Modular Armour Illusion System and general movement controls in a testlevel. It cannot yet be estimated when this first demo can be published. 
 

## Priorities

```
1. Design Documentation
2. Modeling - Programming - Animation
3. Scripting - Spacering - Supportive Writing
    1. Starting Routines / NPC Placement
    2. Guild Plots
    3. Main Plot
```

### Priority I

Finishing the documentation of our world design, gameplay mechanics and features, animations and music is of the highest priority in order to support and accelerate (or even just enable) the work on these areas and do so most effectively and according to plan.  


### Priority II

World Modeling, Programming, Animation, Music: We list these as priority number 2 since all of these areas either are already or could be perfectly worked on simultaneously by different people without interfering with one another. 

**World Modeling:** As long as major parts of the world are under construction, the waynet and waypoints may change (the invisible net of single points that are used to control the positioning and movement of NPCs). It does not make sense to focus on scripting until the world modeling is done. Therefore Flosha is currently focused on the world modeling. He is working on it alone. 

The Colony design takes precedence over the design of the outside world areas and the City design, but since inspiration is a major factor that can motivate and speed up the work, he is working on what is currently most motivating to work on. Switching between the colony design (which is a very restricted work based on our sources) and the city design (where we have a lot of freedom to design what we want) means variety and is a motivating approach. 
{: .subtext }

**Programming:** Auronen is working on tools related to compilation and engine related stuff. Our gameplay features we are planning for Phoenix either are or will be based on this work. 

**Animation:** We need someone experienced with character animation who wants to help us to fix or reconstruct alpha animations to make them useable with the newer rig, as well as to improve animations and create new animations in regard to new movement mechanics. 

**Music:** We currently have no composer actively working on music for Phoenix. Some of the old music has to be remixed, other music has to be created from scratch; background informations and instructions are given. You will fit perfectly if you like both the [Gothic/Alpha Soundtrack](https://gothicarchive.org/music/) as well as ambient music in the style of STALKER ([Example 1](https://m.youtube.com/watch?v=Y0x5UZzX3kQ&pp=ygUSc3RhbGtlciByYXJlIG11c2lj#searching), [Example 2](https://m.youtube.com/watch?v=gjf_VfZFwRg&list=PLS0H674D7-s7DEhmIzYSE-FxIIe_y-yGQ&index=22&pp=iAQB8AUB))
and heavier electronic, industrial music in the style of oldschool shooters like Quake. If you can reproduce music in a similar style and like the idea of a mixture of these - you are highly welcome to contribute. <!-- Your work may greatly influence the atmosphere of the Orc Caves, the Ancient Temple and of the City Khorinis. -->


### Priority III

**Writing:** Story writing in regard to the main plot is currently not needed. It has been written by Flosha and logx and is mostly done.  
Supportive writing such as for ingame books, ambient dialogues, preachings as well as mission/quest ideas are always welcome. In order to contribute in this regard in a way consistent with the Phoenix universe, you should read all of our [/vision](/vision/vision), [/lore](/lore/lore) and [/world](/story/world) documentation first. 

**Scripting:** For the above mentioned reasons, no scripting is currently done and scripters are not needed at the moment. 


## What we did so far

*work in progress, written by memory*

| Year | Our Work, Focus & Publications |
|------|--------------------------------|
| 2016 | The project is started by Flosha under the working title *Nyx*. Story-writing is started. First exchanges with logx. |
| 2017 | Flosha re-models the entire Old Camp of the Sequel based on Screenshots. May: logx (Oliver) officially joins the team. The first guild plots are started to be developed. November: Official founding of [PhoenixTales](https://phoenixtales.de). |
| 2018 | The first version of the story of Act II is completed. The first rudimentary form of an internal Archive is starting to form. Basic lore development. |
| 2019 | We realise the work is impossible to pull off without really being able to comprehend all the material in question. Flosha sets up the Gothic Archive as an internal archive for Phoenix for the sighting of Pre-Release material alongside a simple website that didn't found much interest as there were no graphical image links (v0.1 to v0.4); he then decides to make it public in form of a new website for the community including the graphical navigation (v0.5). Arbax (Dortman) joins the team as a supportive writer. Pixel by pixel reconstruction of the original Gothic Alpha Ingame Font by Flosha. |
| 2020 | Release of the [Gothic Archive](https://gothicarchive.org) (v0.5) in March 21th. Gothic v0.56c and v0.64b are handed over to PhoenixTales. We publish the Phoenix Pitch from 1997. We release an updated version of the Gothic MDK. Flosha writes a new website of the project under [phoenixthegame.com](https://phoenixthegame.com) and sets Phoenix to be the new name of the project. It is published at December 24th. Avallach (Adam) joins the team. |
| 2021 | Flosha [visits Mike Hoge](), who hands over all of his remaining design concepts for digitisation, which Piranha Bytes wanted to throw away. We release them in the archive from march 15th to april 15th and in the following year. Among them hundreds of unreleased concept arts, handwritten design documents and an entire [Gothic Novel]() by Alex Wittmann, once supposed to be released as an official book. Another former developer sends us the "Phoenix Main Mission" document. Reconstruction of the original Alpha Fonts by Pierre. Creation of diverse lacking transitional textures. Tweaking of the camera perspectives. First attempt to harmonise the Alpha Troll Canyon with a Pass and the "Saturas hill". Mage's Chapel Overhaul. Baron's house overhaul. Arena overhaul. First implementation of the northern forest. The overhaul of the southern environment of the Colony begins. Overhaul of the marketplace. Implementation of a new body & head texture system by Sasha (jr) to enable us to use a more systematic naming scheme and make character individualisation easier. Implementation of FogZones by Pierre. Avallach writes a new Archive backend split in several repos to improve the very long page building loading times and enable a simple download of the Archive. logx retires. | 
| 2022 | Auronen (Jan) joins the team as a programmer (21/1/2022) and writes a first version of our inventory and item handling system. We are given the Story v3.3 documentation and an additional collection of 14 Phoenix documents. They are released in the Archive at June 27th. The Mad Scientists provide us with the [Finster Demo](https://gothicarchive.org/demos/finster/). Vaana makes it work on modern systems and we release it in the Archive three months later in September 17th. |
| 2023 | Flosha and Avallach visit Mike again to return the design documentation. We publish the Gothic Comic and are given the original Comic pencil drawings. Flosha decides to realise the Phoenix Documentation in a similar way as the Gothic Archive, as a public website to facilitate contributions, exchange of ideas and the conservation of our gamedesign ideas. The [Phoenix Concept](/) website goes online at May 14th. |
| 2024 | The model on the city and its environment continues. The focus lies completely on the design documentation, on writing new documentation based on all the newly acquired material and the sighting and transfer of all of our chaotic design notes from the first years of conception in a clear and structured way into the public Phoenix Concept (except for the plot documentation, which is written in a private repo). Hagen (Robert) joins our team in September. |
| 2025+ | Hopefully a tech demo focusing on gameplay mechanics. |

```
Clarify:  
1. When did I reconstruct the western plateau?
2. When did I reconstruct the monastery ruins?
3. When did I start modeling the city?
4. When did I decide to include the city?
5. When did I decide to make it a single drama?
6. What did we write when in 2016-2019?
7. When exactly did Arbax and Adam join?

Todo:
* Months may be added.
```

<!-- 
## Priorities

We will list our priorities split into different areas.

* **Documentation:** We try to rewrite, translate (from German to English) and bring over all the design documents written since 2016 into our public Phoenix Concept as well as finishing all the required additional research that we have to do due to the plethora of design documents we received; the study and documentation and especially harmonisation of which is taking a lot of time. This work is done by Flosha. 

* **Modeling:** In the modeling the colony has priority over the outside world and the city. The main focus of the modeling in the colony is now the northern environment, where we aim to harmonise a lot of contradictory ideas. Then we will go back to the southern environment where we need to fix and improve upon a few things. The rock cemetary and the area around the Free Camp is almost finished, but also requires tweaking and more details. At the end we will approach the overhaul of the East with the new swamp as imagined in the Alpha concepts. As for the camps: The Old Camp is almost finished except for details at the Barons house and the three additional prison levels. The New Camp model is almost done but mapping remains. The Free Camp may be done 50%. The Psi Camp is at the stage of the 0.64b Alpha, but requires additional work based on Ralfs concept arts. The outline of the city and the basic locations are set, but due to all the planned verticality, due to the necessity of making every single building theoretically accessible and so on, the remaining work load is still immense. Most work went into the Varantinian quarter (maybe done to 30%) and the Slums so far which may be done to 60-70%. The ghost district and the older parts of the city are still very barebones. The Abandoned Factory is done to ~80%. The forest modeling has not been started other than its vast outside shape. The ricefields at the city are at 10%. This work is also done by Flosha. 

* **Programming:** We want to release a first Pre-Alpha Demo focused on Item Handling, Inventory, our Modular Armour Illusion System and general movement controls in a testlevel. Auronen is working on this. But due to lack of time help of additional passionate programmers may be needed.

* **Scripting:** There is no scripting to do before the world is modeled completely. 

---

-->


<style>

    .roadmap {
        border: 5px solid var(--swamp);
    }


    .article ul {
        padding-left: 0;
    }

    .article ul li {
        background: var(--water);
        border: 6px solid var(--water);
        list-style: none;
        padding: 0.5em 1.5em;
        margin-bottom: 1em;
        font-size: 14px;
        font-family: monospace;
    }

        .article ul li:nth-of-type(even) {
            border: 6px solid var(--darkblood);
            background: var(--darkblood);
        }

        .article ul li strong {
            font-weight: normal;
            text-transform: uppercase;
        }

    

    .article table {
        max-width: 100%;
        font-size: 14px;
        margin: 2em 0;
        padding: 1em;
        overflow: auto;
    }

    table, th, td {
        /* border: 1px solid var(--stone);*/
        border: none;
        border-collapse: collapse;
        padding: 1em;
    }

    table tr td:nth-of-type(odd) {
        background: var(--water);
        text-align: center;
        font-family: monospace;
    }

    td {
        overflow: auto;
    }

    th {
        background: var(--darkblood);
        font-family: monospace;
        text-transform: uppercase;
        font-weight: normal;
        font-size: 14px;
    }

    tr:nth-of-type(odd) {
        background: var(--darker);
    }

    tr:nth-of-type(even) {
        background: var(--darkest);
    }
    

</style>
