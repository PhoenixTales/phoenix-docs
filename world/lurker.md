# Snapper & Lurker

*flosha*, 06.03.2025

In the release version of Gothic, Lurker and Snapper are two different creatures with no relation to each other. Originally they were one and the same.

> **Mike Hoge:** [...] one cool monster is the snapper. It can swim and dive as well as walk on the land. Like in Ultima Underworld, there is much water in our dungeons. Sometimes, if you come too close to the shore, it could happen to you, that suddenly a snapper leaps out of the dark water and eats you (what a pity) but you can do something about it: a) become better (which won't help you in the first place) and b) kill a goblin (snappers like them for breakfast) and throw it in the lake - if there's a snapper in it, it will be preoccupied and you can swim through the lake, if not, a goblin dies senseless (again, what a pity). [[src]](https://gothicarchive.org/interviews/1999/16.10.1999_glideunderground.com.txt)

In order to understand our design decisions in regard to these two monsters, we have to go back to the beginning and explain how they came to being.

The original idea was to have a water monster, such as a crocodile. But just as with almost all the other monster designs, the idea was to divert from common fantasy universes as well as from reality by a more unique design.

In this context, some relevant quotes from the [Monsters document](https://gothicarchive.org/documents/phoenix-docs) of the original Phoenix Concept:

> Der Snapper lebt größtenteils im Wasser. Kann an Land springen und angreifen. Im Wasser praktisch unbesiegbar, muß vom Land aus bekämpft werden. Wassermonster verstecken sich auf dem dunklen Grund eines Gebirgssees oder unter Felsvorsprüngen unter Wasser. Schlägt etwas auf die Wasseroberfläche, greifen sie blitzschnell an. Ein ins Wasser geworfener Stein lockt sie an. 

> Snapper schwimmen ähnlich wie ein Krokodil. Meist tauchen sie aber. Erst wenn sie durch etwas angelockt werden (z.B. Steinwurf), schwimmen sie kurze Zeit an der Stelle des Auftreffens im Kreis, bevor sie wieder Abtauchen. / Snapper können unbegrenzt tauchen. Sie tauchen wesentlich schneller als alle anderen Spezies. Sie können auch während des Tauchens angreifen. Dazu schnellen sie vor und beißen das Opfer. 

It would swim and dive in the water and attack the player when swimming and diving. And when the player would walk by some pond, he would suddenly "snap" out of the water with a jump attack to get him and pull him into the water. Therefore, this monster was called "Snapper". 

![Vadims Frog](https://images.gothicarchive.org/conceptart/vadim/old/snapper01a.jpg)

Due to this idea for the monster, as being in the water, but close to the water's edge and as being able to jump, they thought: How to design such a monster in a unique way? Vadim, who was initially responsible for the monster design, came up with the idea of a giant frog with sharp teeth. The frog made sense because he could jump and his legs have developed accordingly. 

But for some unknown reasons this design was discarded. The initial idea of a giant frog may have found a similar expression in form of the Orc Dog from the Alpha, basically a "mouth on legs" (see Orc Dog). And as the water monster, called Snapper at the time, this monster was designed:

![0.5 snapper](https://images.gothicarchive.org/research/056c-monsters/Snapper_P1.png)

While the model has some resemblance to the former frog concept, the texture shows that they decided against the frog approach. This snapper was blue, as he was in the water and had big hind legs to jump. But overall he already looked more like the Snapper of the release version.

But this approach was discarded too, instead a new monster was designed: the Lurker. Like the Snapper, the Lurker was meant to be blue/green and only come at land to attack (please be aware that of course this texture below was a placeholder). He too has a still a bit of resemblance to the frog concept, but overall diverts from the idea. He had similarly large hind legs, but bigger front legs too, walking on all fours and the head and mouth was given a more elongated shape. Overall, the Lurker brought the design a bit closer to the crocodile, the "regular" water monster that they wanted to divert from in form of a unique fantasy design, but with longer legs due to the jumping idea - a crocodile cannot jump. 

![0.6 Lurker](https://images.gothicarchive.org/research/064b-monsters/Snapper_Perspective.png)

While the Lurker replaced the Snapper as the water monster, they didn't want to ommit their former Snapper idea and developed it into what is known from the release version (where the snappers, while not *in* the water, are still hanging around *at* the water, e.g. at the pond below the Demontower). Since he was not in the water anymore the blue colour didn't fit and so the design was basically changed into that of a regular (to not say boring) dinosaur (as imagined at the time and as presented e.g. in Jurassic Park - today we know thay dinosaurs looked much different). In this aspect they diverted for the first time from their own goal of having no common real creatures nor conventional fantasy monsters. 

![0.7 Snapper](https://images.gothicarchive.org/artworks/monsters/der_neue_Snapper.jpg)

But then, in course of development, the idea of a monster diving and attacking the player inside of the water as well as the idea of jumping/snapping out of the water couldn't be realised, be it due to technical complications or lack of time or both. This was basically the end of the whole idea of the water monster. 

In consequence the Lurker too was put on the land, at the edges of water, opposed to the very idea inspiring his name of "lurking" inside of the water. And like the Snapper his skin was also changed in colour to a tone more akin to the beaches at which he would hang around. 

![Vanilla Lurker](https://images.gothicarchive.org/artworks/monsters/12.jpg)


## Summary

The very idea of a water monster inspired both the Snapper and the Lurker, but in the end none of them fulfilled what they were meant to do. Due to this development, whatever the reasons may be, we ended up with two monsters that did not fulfill their purpose. Neither did we end up with a monster that would *snap* out of the water like a frog, nor did we end up with a monster that would silently *lurk* in the water like a crocodile. 

We got two very different monsters instead, one a stereotypical dinosaur, one a halfway unique creature that doesn't know if it wants to be a crocodile or a frog and sounds like a dragon when it attacks. To make it short: I am not convinced. 

In the attempt to design a water monster and to preserve different interesting monster designs, the original idea and purpose that every monster should have in the world, has been lost (as in other cases too). And by the combination of the different characteristics (frog/croc) and the inability to realise the required AI for the monster to function as imagined, the potential and meaning of both ideas was reduced instead of highlighted.

Therefore we approach it in the opposite way. Due to the goal of our project of realising the old ideas, we have to include the water monster as originally announced. And instead of trying to combine the two inspirations and ending up with no water monster at all, we may keep them seperate and design two:
* The Snapper, inspired by a frog, inhabiting ponds and more shallow water, snapping out of the water with a jump attack with the necessarily powerful legs. 
* The Lurker, inspired by a crocodile, inhabiting rivers and deeper waters, lurking in the water to silently approach its prey on all fours, with shorter legs - which also requires a different sound design.

These two monsters replace the Lurker and Snapper as presented in the release version, as they aren't serving the desired purpose, are too stereotypical in appearance (in case of the Snapper) and just add an unnecessary and less believable (to not say chaotic) complexity to the wildlife of the small colony, which will become more clear when you read our notes about the other monsters in the world of Gothic. 
