# Materials

*Flosha, 05.09.2025*


## Introducing a new "Swamp Water" material

In the ZenGin, different materials are used in order to change the behaviour of a given triangle in the world model (polygons, of which the model consists) to behave differently. For example, a grass material will result in a different foot step sound effect than stone or wood. A special kind of material is water. By assigning this material, the player will no longer be able to walk over the plane, but through it. In case of water, he will walk, run and sprint normally through the plane as long as he is not "too deep" in the water. If he reaches a specific depth, he begins to wade through the water, in a wading animation, which is making him much slower. And if he reaches the next depth defined in the engine he will begin to swim and not walk further (otherwise he would start walking underwater and drown). 

In order to realise the swamp as we would like to and as it would give justice to it, we have to give swamp water a different behaviour than normal water. 

(1) Instead of letting the player wade through the water only if he reaches a depth to e.g. his knees, in case of swamp water the player will start to wade immediately (or after just a few cm, e.g. feet depth), because it is sticky and slows him down. Then, instead of swimming, when he continues to walk further into the swamp, he keeps wading and cannot swim. When his head starts to come closer to the surface, he starts to hold his arms up and the player should be able to recognise that it becomes dangerous now. If he goes yet further and the head goes under the surface, he drowns. This is how it should work in case of going into the swamp on a declined plane. 

(2) But what if the player "falls" into swamp water and into an area that is so deep that he would be "under water" immediately? In this case, the fall should somehow be decelerated drastically. Depending on the height from which he falls into the water, this deceleration should be more or less. But he should always be somewhat decelerated in his fall when falling into swamp water (much deceleration if he just e.g. falls into it from a few cm or half a meter. Much less deceleration if he falls from 5+ meters. Nonetheless, if falling into swamp water that is as deep that his head will end up under water, he will always be pulled into it and drown; in such a case, we need a new animation of him struggeling in the water and trying to get out, but being constantly pulled deeper into it. 

