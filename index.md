# Introduction

<img class="phnx-mask" src="/_img/phnx-mask-v07-retro.png">
<img class="logo" src="/_img/headings/designdocs2.png">

*Welcome to the desert of the ideal.*  

These are the Design Documents of [PHOENIX](https://phoenixthegame.com) (working title "Project Nyx"), a radically immersive action rpg developed by Phoenix Tales, based on GOTHIC (2001) by Piranha Bytes which had "Phoenix" as its working title. GOTHIC was supposed to be very different in 1996-1999. The release version was a mere fracture of what they had initially dreamed of and the vision was severely compromised. PHOENIX is an attempt to realise this dream. 

```
"Phoenix Design Concept"
2016-2024 by PhoenixTales

Authors: 
Flosha, logx, Phantom95
Arbax, Avallach, Auronen
```  

In the early stages of development we created what later would become the [Gothic Archive](https://gothicarchive.org) by collecting as much pre-release material as possible to research the original vision of what we summarise as the “Gothic Alpha”. In the course of this work we decided to prepare and present it in the form of a website to the community.

All the research of said material and our own game design derived from it are extensively documented in the design concept at hand. In the same way as we have made our Archive public source we have also decided to release our design docs in the form of a website. It is our own minimal online documentation solution, where the index serves as the navigation. Documents are written in markdown and are automatically formatted as HTML, often complemented by spreadsheets appended. It is easy to contribute [via git](https://github.com/PhoenixTales/phoenix-docs), so everyone can collaborate with us in our research. Since we target an international audience and are an international team <!--(from Germany, Poland, Romania, Czechia and with associations to Ukraine, Russia and Slovakia)--> we write the documentation in english.  

A long-term goal is a physical publication of the concept after the release of the game.   


## Document Structure

While working on our design docs we had to come up with a way to structure the documentation, as you see it in our main index. The documentation is extremely comprehensive and complex and there would be a myriad of ways to structure it. We wanted the structure to be simple and straightforward. Therefore the concept is divided into just three main sections: Vision, Mechanics and Story (+ appendices). 

<p class="subtext blueinfo">Please note that the Design Concept is an ongoing documentation of the project since 2016. It is <strong class="demonic">work in progress</strong>. Many documents are currently rewritten and will be unlocked over time. Due to the current work on the order and internal structure of the documents, regular changes to the index are to be expected.</p>

Current structure:  

```
DESIGN CONCEPT

1. Vision 
2. Mechanics
3. Story
   4.1 Setting
   4.2 World
   4.3 Relations
   4.4 Plot
   4.5 Missions

APPENDIX
1. Promotion
2. Inspirations
3. Credits
```

Whenever a topic has a source in design documents, old builds of the game or both, our documentation is structured in an "Alpha" and a "Phoenix" section:  

```
(1) Research of how aspect X was planned  
(2) Concept for realisation of X in Phoenix
```

**Author:** Flosha  
**Written:** 14.05.2023   
**Changed:** 15.05.2023  


## Support

Please note that [Phoenix](https://phoenixthegame.com), the Phoenix Documentation at hand and the entire [Gothic Archive](https://gothicarchive.org) created alongside the project are being done non-commercially and primarily by one person at his free time. At the same time domains and backup storage have to be paid. If you want to support us or just give something in return for the work on the game, the Gothic Archive and this documentation, you can do so [via ko-fi](https://ko-fi.com/flosha).


## Read next 

* [Vision](/vision/vision)


## Links

* [phoenixtales.de](https://phoenixtales.de)
* [phoenixthegame.com](https://phoenixthegame.com)
* [gothicarchive.org](https://gothicarchive.org)


<style>

   main {
      background: url("/_img/bg/workbg.jpg");
      background-position: top right;
      background-size: 70%;
      background-repeat: no-repeat;
      width: 100%;
   }
      main article {
         padding-top: 500px;
      }
         main .article h1 {
            font-size: 20px;
         }

   .logo {
      display: block;
      image-rendering: pixelated;
      max-height: 400px;
      max-width: 100%;
      margin: 0 auto 2em;
   } 

   .phnx-mask {
      display: block;
      image-rendering: pixelated;
      margin: 0 auto;
      padding-top: 2em;
      width: 450px;
   }

   @media only screen
   and (max-width : 820px) {

      main {
         background: none;
      }

      .phnx-mask {
         width: 100%;
      }
   }
</style>