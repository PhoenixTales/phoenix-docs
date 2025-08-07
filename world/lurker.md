# Snapper & Lurker

*flosha*, 06.03.2025  
last update: 08.03.2025  

In the release version of Gothic, Lurker and Snapper are two different creatures with no relation to each other. Originally they were one and the same.

> **Mike Hoge:** [...] one cool monster is the snapper. It can swim and dive as well as walk on the land. Like in Ultima Underworld, there is much water in our dungeons. Sometimes, if you come too close to the shore, it could happen to you, that suddenly a snapper leaps out of the dark water and eats you (what a pity) but you can do something about it: a) become better (which won't help you in the first place) and b) kill a goblin (snappers like them for breakfast) and throw it in the lake - if there's a snapper in it, it will be preoccupied and you can swim through the lake, if not, a goblin dies senseless (again, what a pity). [[src]](https://gothicarchive.org/interviews/1999/16.10.1999_glideunderground.com.txt)

In order to understand our design decisions in regard to these two monsters, we have to go back to the beginning and explain how they came to being.

The original idea was to have a water monster, e.g. something comparable to a crocodile. But just as with almost all the other monster designs, the idea was to divert from common fantasy universes as well as from reality by a more unique design.

In this context, some relevant quotes from the [Monsters document](https://gothicarchive.org/documents/phoenix-docs) of the original Phoenix Concept (I translate them from german):

> Der Snapper lebt größtenteils im Wasser. Kann an Land springen und angreifen. Im Wasser praktisch unbesiegbar, muß vom Land aus bekämpft werden. Wassermonster verstecken sich auf dem dunklen Grund eines Gebirgssees oder unter Felsvorsprüngen unter Wasser. Schlägt etwas auf die Wasseroberfläche, greifen sie blitzschnell an. Ein ins Wasser geworfener Stein lockt sie an.

> EN: The Snapper lives mostly in the water. At land he can jump and attack. In the water he is practically undefeatable, must be fighted on land. Water monsters hide on the dark ground of a mountain lake or below rock spurs under water. If something hits the water surface, they attack at lightning speed. A stone thrown into the water allures them.

> Snapper schwimmen ähnlich wie ein Krokodil. Meist tauchen sie aber. Erst wenn sie durch etwas angelockt werden (z.B. Steinwurf), schwimmen sie kurze Zeit an der Stelle des Auftreffens im Kreis, bevor sie wieder Abtauchen. / Snapper können unbegrenzt tauchen. Sie tauchen wesentlich schneller als alle anderen Spezies. Sie können auch während des Tauchens angreifen. Dazu schnellen sie vor und beißen das Opfer.

> EN: Snappers swim similarly as a crocodile. But most of the time they are diving. Just when they are lured by something (e.g. stone throw), they swim for a short time in a circle around the position where the water was hit, before they dive down again. / Snappers can dive indefinitely. They dive much faster than every other species. They can also attack during diving. For this they spring out and bite the victim. 
 
It would swim and dive in the water and attack the player when swimming and diving. And when the player would walk by some pond, he would suddenly "snap" out of the water with a jump attack to get him and pull him into the water. Therefore, this monster was called "Snapper".

![Vadims Frog](https://images.gothicarchive.org/conceptart/vadim/old/snapper01a.jpg)

Based on this idea of a monster, as being deep in the water, but also lurking close to the water's edge and as being able to jump, they tried to come up with a visual design. Vadim, who was initially responsible for the monster design, came up with the idea of a giant frog with sharp teeth. But the first model of the Snapper that we know of, appeared in v0.5: 

![0.5 snapper](https://images.gothicarchive.org/research/056c-monsters/Snapper_P1.png)

On first sight it doesn't seem to have too much resemblance to the frog idea, because the proportions are so different. The head is much smaller, the body longer. And in this regard it comes closer to the crocodile than the frog, or, to be more precise, to a salamander.

The frog made sense because he can jump and his legs have developed accordingly, but he wouldn't be able to swim as fast and to attack as suddenly during diving. For this a longer spine was needed. In this senese we can say that the frog idea was developed further into the idea of a mixture of Salamander and frog. He would move underwater as fast as a Salamander or Crocodile, and at the same time be able to jump on land like frog or toad.

The initial idea of a giant frog may have found expression (proportion-wise) in form of the Orc Dog from the Alpha, basically a "mouth on legs" (see Orc Dog). 
{: .subtext }

The texture of this first known Snapper model seems actually to be inspired by and trying to replicate the frog idea to some degree, even if it may be hard to see on these old and small textures. In difference to a crocodile, it does not come with visible scales, but the overall dark skin (ignoring the blue shiny parts) remind most of the uneven skin of a toad or specific types of salamanders. With the blue parts, which to be honest, appear a bit like some harder, crystal like material, it seems that they've designed them as such to let the skin there appear to be wet and glossy like that of a frog or again, a salamander.  

Other than that they have chosen to make his skin less green and more blue. Both was fine for a water monster. But leaning more towards dark blue than green with some lighter, glossy accents to me seems to be a good decision for a monster that was meant to hide in dark blue lakes (in accordance with the dark blue water texture that was used in the Alpha).

---

It was a good approach. But they seem not to have been quite confident with it and were going to develop it further. A new snapper design appeared in v0.6. 

![0.6 Lurker](https://images.gothicarchive.org/research/064b-monsters/Snapper_Perspective.png)

This model shows what was later to be renamed into a new monster called "Lurker". But at that time it was still called Snapper and was simply what the former design was developed into (please be aware that of course the texture above was most likely a placeholder).

Again, on first sight he looks very different to the former Snapper design, but actually he isn't that much. The form of the head was changed, which just brought it even closer to the lizard/salamander idea and a bit away from the frog. But the large hind legs are almost identical and so is the tail. The overall shape of the body didn't change much. The blue glossy parts are also still there in the model, just appear black in the placeholder texture. 

He was still blue, but with more green mixed in, which appears like the attempt to find a new balanced colour between the former blue Snapper and the green frog.

The biggest difference was that they elongated the arms into very strange, thin front legs to let him walk on all fours when on land, instead of on two legs only, like the old Snapper was moving. This made sense when we speculate that they wanted to bring it closer to a Salamander in appearance, but I would argue that this reasonable intention was badly executed.

Instead of elongating the arms, first and foremost they should have changed the posture of the monster and let it move much closer to the ground, which would fit much better to a water monster and let it seem more dangerous too. Similar to a crocodile it would run towards the player from this low, lurking position and for the jump attack it would thighten together and prepare for a jump similar to a cat before jumping on its prey. 

In this case the walking animation would have had to be different too, more akin to how salamandars or frogs are walking instead of almost like a dog without "elbows" as the Snapper (later "Lurker") from v0.6 onwards. 

---

It seems that they didn't want to give up on the older Snapper design though and thus renamed the Snapper into "Lurker" and a new Snapper appeared, as known from the release version (where the snappers, while not *in* the water, are still hanging around *at* the water, e.g. at the pond below the Demontower). 

Since he was not in the water anymore the blue colour didn't fit and so the design was basically changed into that of a regular (to not say boring) dinosaur (as imagined at the time and as presented e.g. in Jurassic Park - today it is said that dinosaurs looked quite different). In this aspect they diverted for the first time from their own goal of having no common real creatures nor conventional fantasy monsters in the colony. 

![0.7 Snapper](https://images.gothicarchive.org/artworks/monsters/der_neue_Snapper.jpg)

But then, in course of development, the idea of a monster diving and attacking the player inside of the water as well as the idea of jumping/snapping out of the water couldn't be realised, be it due to technical complications or lack of time or both, which marked the end of the whole idea of the water monster. 

In consequence the Lurker too was put on the land, at the edges of water, opposed to the very idea inspiring his name of "lurking" inside of the water. And like the Snapper his skin was also changed in colour to a tone more akin to the beaches at which he would hang around. 

![Vanilla Lurker](https://images.gothicarchive.org/artworks/monsters/12.jpg)


## Summary

The very idea of a water monster inspired both the Snapper and the Lurker, but in the end none of them fulfilled what they were meant to do. Due to this development, whatever the reasons may be, we ended up with two monsters that did not fulfill their purpose. Neither did we end up with a monster that would *snap* out of the water like a frog, nor did we end up with a monster that would silently *lurk* in the water like a crocodile. 

We got two very different monsters instead, one a stereotypical dinosaur, one a halfway unique creature with unconvincing features.

The idea of a water monster as a mix of giant frog and salamander would have been in accordance with the design principles and Mikes philosophy of a good/new idea consisting of the combination of two elements that were not combined before. It would have presented us with a really unique monster design. The final design did not fulfill this ideal. 

In the attempt to design a water monster and to preserve different interesting monster designs, the original idea and purpose that every monster should have in the world, has been lost (as in other cases too). And by the combination of the different characteristics (frog/croc/lizard) and the inability to realise the required AI for the monster to function as imagined, the potential and meaning of both ideas was reduced instead of highlighted.

Due to the goal of our project of realising the old ideas, we have to include the water monster as originally announced. 

We have to go back to the Snapper design from 0.5 and 0.6, harmonise and improve upon them, in order to execute the idea in a more unique and reasonable way, by following the salamander-frog idea. 

This Snapper/Lurker haa to be able to both snap out of the water with a jump attack with the necessarily powerful legs as well as lurk in the water to silently approach its prey on all fours, with shorter legs (which requires different walking animations and a different sound design), as well as attack during diving at lightning speed. 

This monster replaces both the Lurker and the Snapper as presented in the release version, as they aren't serving the desired purpose, are too stereotypical in appearance (in case of the Snapper) and just add an unnecessary and less believable (to not say chaotic) complexity to the wildlife of the small colony, which will become more clear when you read our notes about the other monsters in the world of Gothic. 

[Todo: Add our Snapper design]
