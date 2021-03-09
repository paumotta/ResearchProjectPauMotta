# ResearchProjectPauMotta

##_Index_
-
##_1.History of AI_

###_1.1. Deep Blue_

###_1.2. Monte Carlo Tree Search Method_


##_2.Ai and immersive gameplay_

###_2.1. Game Façade_

Façade is an artificial-intelligence-based interactive story created by Michael Mateas and Andrew Stern. It was the winner of the Grand Jury Prize at the 2006 Slamdance Independent Games Festival and has been exhibited at several international art shows. 
Façade’s AI analyze what the player writes and create new responses. For example in some scenarios Grace may respond favorably to the statement 'I love your decorations.', while in another context she may believe you are being condescending to her. 
Façade coordinates the AI with the “Drama Manager”. It figures out where the plot goes depending of what happened and how each character is “feelings”. The tension between them including you (the player) as the main influencer on each character issues.


###_2.2. Doom_

Doom (stylized as DooM, and later DOOM) is a video game series and media franchise created by John Carmack, John Romero, Adrian Carmack, Kevin Cloud, and Tom Hall. The series focuses on the exploits of an unnamed space marine operating under the auspices of the Union Aerospace Corporation (UAC), who fights hordes of demons and the undead.
This game is famous by its unique combat system, Push Forward Combat where the player would be driven forward instead of boing forced into cover. In addition, that was a guide for all aspects on the game, including level design, narrative and player progression. 
On the enemies AI design, the designer’s team describe them as a small palette and simple role. It has to be easy for players to understand (be able to describe them in one sentence) and predictable in their actions in order to be confident enough in that combat.
One example of an enemy that explains very well the idea o push forward combat is the Imp.

<<Imp>>

Its role is quite obvious from silhouette and teaches the player that have to dodge his projectile. Moreover, their small size and jumpy nature makes players caches after them.

###_2.3. Left 4 Dead_

Left 4 Dead is a 2008 multiplayer survival horror game developed by Valve South and published by Valve. It sets you in a zombie apocalypse with the goal to reach the end of the map.
This excited and stressful gameplay is driven by the Left 4 Dead Director, an AI agent who manipulates what is happening on the scene depending on the skill of the player and the stress level of the player, composed by the number of zombies attacking, the proximity to the player (if they are closer to you, you will be more stress) and is some special enemy is attacking the player. The AI system measures each player stress level meaning that the director will focus on player which stress levels are lower than others.
This is a crucial component of the game because reinforces the idea of you can’t stay on the same place for too long, there is a need to keep moving and pay attention to what is happening around you.

###_2.4. Alien: Isolation_

Alien: Isolation is a 2014 survival horror video game developed by Creative Assembly and published by Sega originally for Microsoft Windows, PlayStation. Based on the Alien science fiction horror film series, the game is set 15 years after the events of the original 1979 film Alien, and follows engineer Amanda Ripley, daughter of Alien protagonist Ellen Ripley, as she investigates the disappearance of her mother.
The Xenophormer was built in the idea of the “pshycopath serendipity” which the alien always find itself in the right place at the right time. Even if you’re in hiding and the monster can’t see you, and it doesn’t know your ultimate goal, it will still find a way to mess with your plans. 
The unique part of this game is the powerlessness of the main character, you cannot kill the alien, which means you have to find ways to avoid the direct contact with her.
In order to create and AI that suits on the type of game they were looking for. To achieve this, the game uses 2 different behavior management system: The Macro AI and the Micro AI. The Macro AI is the director, which observes the player all the time though the game, meanwhile the Micro AI is seated on the Alien itself. The director’s job is to point the alien in the direction of the player periodically, to give it a hint as to where it should be looking. Despite this, the alien is never allowed to cheat: while the director always knows where you are, the alien has to figure it out for himself. 
While the alien is near the player, the menace gauge would increase depending on specific factors:
-	Whether the creature is within a short walking distance of the player.
-	Whether the player has actual line of sight on the alien.
-	Whether the alien was close on the motion tracker, but could also reach the player quickly.
The last item is particularly important, as the alien could technically be close on the motion tracker but in another room. As such, the threat won’t increase at the same rate given the threat is minimal.


##_3.Designing battle AI_

###_3.1. Finite-state Machine (FSM)_
A finite-state machine is a model used to represent and control execution flow. It is perfect for implementing AI in games, producing great results without a complex code.
A finite-state machine is a model of computation based on a hypothetical machine made of one or more states. Only a single state can be active at the same time, so the machine must transition from one state to another in order to perform different actions. Transitioning depending of which trigger was active.
 
An FSM can be represented by a graph, where the nodes are the states and the edges are the transitions. Each edge has a label informing when the transition should happen, like the player is near label in the figure above, which indicates that the machine will transition from wander to attack if the player is near.
Some examples of an FMS in games are the Pacman enemies were each of them have a specific behavior. Nevertheless, when Pacman eats a power pallet their behavior changes. 

###_3.2. RPG Battles_

When we design PRG Enemy AI we need to take into account what type of entity we are doing, is a melee character, a range character or a supportive character. Moreover, we need to think is some of these characters have skills that can be used on combat or not. 
In some RPG Turn base combat the enemies knows about the opposing party members in order to select the target to attack. There are few logics that we can use to determine the attacker’s target. The closest to the attacker, the farthest to the attacker, the one with most current HP, the one with the least current HP, always attack a specific type of the party member.
The next step is to attack, this can be a normal attack or a skill. Each attacker will have a different percentage between a normal and skill attack, some will use normal attack more often others will use more skill based attacks. Of course, in case of skill based attacks, we will first check whether or not the attacker’s current SP is sufficient for the attack or the skill is on cool down.
For example, the Epic Seven is a mobile game RPG Turn Based Combat where each enemy have their own type of logic. Despite of the enemy AI will always attack a random target but the unit that is placed in the front has the highest chance of getting attacked. Some enemies will always use a basic attack. If there are a special boss the first attack they will be a skill.


##_4.Bibliography_

https://forums.rpgmakerweb.com/index.php?threads/enemy-ai-design.124200/
https://www.youtube.com/watch?v=wh9kpe1Dn8s
https://www.youtube.com/watch?v=POv1cOX8xUM&t=516s
https://www.youtube.com/watch?v=2KQNpQD8Ayo
https://www.youtube.com/watch?v=WbHMxo11HcU
https://gamedevacademy.org/construct-2-rpg-tutorial-designing-the-battle-ai/
https://en.wikipedia.org/wiki/Alien:_Isolation
https://www.youtube.com/watch?v=Nt1XmiDwxhY
https://www.gamasutra.com/blogs/TommyThompson/20171031/308027/The_Perfect_Organism_The_AI_of_Alien_Isolation.php
https://becominghuman.ai/the-perfect-organism-d350c05d8960
https://gamedevelopment.tutsplus.com/tutorials/finite-state-machines-theory-and-implementation--gamedev-11867
https://game8.co/games/Epic-Seven/archives/275491#hl_2
