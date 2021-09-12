---
title: Bee Game Postmortem
---

Hi there! As the title would suggest, today I'll be writing about the very vaguely named Bee Game, my second round at making another cool game at university, but this time with a bit of a different development story. If you like bees, games, or both, read more below!

![Bee Game's Logo]({{ page.dir }}logo.png)  

### Background

After having a lot of fun with putting together Pet Power Down (see the previous project write-up), I decided to mix things up next semester by joining the University of Michigan's game development club: WolverineSoft Studio (for class credit, of course, taken during the 2020 Winter semester, or January-April). Given that I was new to Unity (outside of poking around with it a bit before), I had the choice between joining the main team to work on their big project, or joining the smaller "WolverineSoft Lab," where lab students got put together into smaller teams to work on their own, smaller projects as a team where nobody had a lot of experience. Being able to work through a team where I knew my ideas would actually matter. Naturally, I went with the labs since it sounded more fun as a first-timer, but things didn't quite go as planned.  

Teams got put together after pitches happened, and I ended up pitching 2 ideas, but the one that stuck was the original concept for Bee Game. One real nice way to explain it is that it's like PvP Plants vs Zombies, but instead of zombies you have another player who also uses plants. In other words, players try to launch attacks against their opponent's defenses while the opponent does the same. Each player fights with units the can 'hire' using a currency over timed, and the person who comes out on top is the one who lands enough attacks past the opponent's defenses through a mix of good resource management and smart strategy. Below is an early concept I threw together in GameMaker Studio 2 before I shelved the idea until the chance to build it out again in the WolverineSoft Labs.  

![An early concept for Bee Game from well before development]({{ page.dir }}early_concept.png)

After pitches were over I ended up with a team of 4, and it seemed like we were all super excited to get to work on the game. With some short brainstorming after pitches, my name of Untitled Bug Game ended up sticking, being a mix of letting us use bugs as the main pieces of the game since there are all sorts of different bugs that can do anything, and the Untitled part came about by being shamelessly stolen from the (famous at the time) Untitled Goose Game. From there the Covid-19 pandemic really started to take hold of the world, so things ended up going pretty south after that. Not too long into weekly meetings for the lab, I quickly became the only one to show up out of the 20ish people that started off on teams. It was pretty disappointing since it seemed like I had a fun team that would be ready to put together a really cool idea for a game, but maybe a week or 2 later it was just radio silence. On one hand it meant I now had to do EVERYTHING on the project, which was a bummer since putting together a working game IS a lot of effort. However, it meant that I got to have a hand in every part of the game development process between making controls and sprites that I otherwise might not have done, and rolling solo also meant that every idea I had got to be in the game, instead of having to settle on something everyone agreed on.  

So there's a bit of the story behind in the game. A game about bugs with a team that turned into a game about bees I made on my own. An interesting twist in development for sure, but hey that just means I have more to write about here I guess. So with that background out of the way, let's get into the development.

### Early steps  

Before I get to work on the game past the brainstorming process, I first had to actually learn how to build games in Unity, when Unity isn't exactly beginner friendly... Thankfully, at least at the start of the semester in the labs team, I had some guidance on where to get started. Namely, [Unity's Roll-a-Ball tutorial](https://learn.unity.com/project/roll-a-ball) to get used to Unity's structure and workflow, and  [Unity's Ruby's Adventure tutorial](https://learn.unity.com/project/ruby-s-2d-rpg?tab=overview) to get me used to working in 2D, since that's what my game would be. They're really not the most exciting games since they're meant to be simple tutorials, so I'll just skip over them here.  

Because I was lazy and putting things off at first, one of the first things I did was get some sprite work done. It sounded like a fun things to do and was fairly low effort, so here's the fun stuff I ended up with along with some UI elements: the bugs! In order, we have a bee, ladybug, ant (???), a grasshopper, a bat, and a butterfly.  

![Spritework for the original group of 6 bugs]({{ page.dir }}bugs.png)  

While all of them certainly look like *something*, the style was a bit all over the place. I thought the bee was amazing, the ladybug was ok but couldn't really be taken further, I'm still not sure that the ant is actually an ant or an alien I drew, the grasshopper looks alright outside of the bored expression I gave it, the bat is way too cartoony, and the butterfly is alright if not a bit plain.  

From there, I started to build out the core of the game. It's been a while so I don't recall the exact all the details in building from there, but it was really just learning as I went. It followed the classic software development cycle of have an idea of what to do, have no idea how to do it, look it up, slap it in, fix what isn't working, and then go back to it later when you realize you can make it work better. After some effort, I managed to apply that process to put together placing units, having them shoot, collision detection to make sure their attacks hit enemies, having units that can die including the player's hearts, and that was it unless I'm missing any smaller stuff. It felt really good to finally be able to apply the ideas of inheritance when building out unit classes for the game for what felt like the first time outside of the classes that say it's super important.  

A side note on the controls: they are super jank. In my head, the game would be a *PERFECT* as a mobile game, where you could have a row of units that you drag where you want them to be as long as you can pay their cost. However, I wasn't about to figure out how to make a mobile game through Unity, let alone game that wasn't local multiplayer since I would be WAY over my head as a beginner for sure. Sure, a mouse would be good substitute, but again we run into a problem with being locked to local multiplayer. Unless you have 2 unique mice as once which is already a lot, you would either have players fighting over who gets to use the mouse or you would just have one player who would be unable to play. Naturally, the next solution would be sharing a keyboard, which is where my control scheme came in, which splits the keyboard for both players. Both players get their own 2x3 set of keys which would allow them to pick which unit to place based on the position they picked, followed by which location on the board. That's a pretty poor description to make out in your head, so just looks at the following screenshots and gameplay. In short, just know that you use the same keys to pick a unit as you do place them, and the keys you use have the same shape the boxes for the board and unit selection, which was intentional.  

Anyways, after finishing up all that I actually had a working prototype! Well, working as in you could place units and have them attack, but still not really a complete game since the graphics needed some touching up and I didn't have a working economy system, so it was just a free-for-all where whoever could place the most bugs the fastest wins instead of who balanced costs against their opponent the best. Still, I actually have a gif of what the game looked like at this point, first using my concept sprites and mouse controls and with the bugs plus the selection UI.

![Gameplay from an early build using the concept assets]({{ page.dir }}early_build_gameplay_people.gif)  
![Gameplay from an early build using the new placement UI and bug assets]({{ page.dir }}early_build_gameplay_bugs.gif)

### Bees? Bees!  

By this point I was getting tired of my bugs. While I loved my bee, all the other bugs looked real bad... Also, trying to make it clear how strong each bug was and what they did different from one another. How does a bee compare to an ant? A ladybug? A grasshopper? It isn't great. Also, how should I even represent their attacks? A bee can shoot its stinger since that would make sense thematically, even if it isn't accurate. Maybe I can have a grasshopper send flying kicks or a bat its teeth, but figuring out the rest would be a struggle. And that's when it struck me: more bees! I knew I could already make bees look good as sprite given my first one, and I had some ideas for fun variations. I opened up my spritework tool and got to work with these results, upscaled from their original 32x32 dimensions:  

![An angry bee with a honeycomb shield]({{ page.dir }}bee_shield.png)  
First, a bee with a shield. Again, I was really happy with this one. Thematically, a honeycomb shield fits pretty well since bees build honeycombs and such, and giving a bee a shield makes it pretty clear that this bee is more defensive than others, which was reflected in the final gameplay.  

![An angry, perfectly normal bee]({{ page.dir }}bee_normal.png)  
Second, our normal bee from before, I believe mostly unchanged.  

![A happy bee on a flower]({{ page.dir }}bee_flower.png)  
Third, a happy honey bee. A big of a different style here, but still a bee. Kind of like Plants vs Zombies, I planned to make a sunflower-esque bee that you invest in to get greater resource production from in the future, which I tried to show through the spritework. An angry bee probably hits harder than a happy one, and it sitting on a flower hopefully gets the idea of pollination across, which comes back to resource production given that honey is the main resource of the game.  

![A angry, perfectly red bee]({{ page.dir }}bee_red.png)  
Fourth, a less creative bee: the red bee. It's a normal bee but red because it is angrier, so it hits harder but also takes less hits. That's really it for this angry bee.  

![A regal queen bee]({{ page.dir }}bee_queen.png)  
Fifth, another fun one, the queen bee! I thought of the queen bee as an upgrade to the shield bee, following the same line of think as before. She's smiling instead of angry, so she probably doesn't hit as hard as others. Also, she's a bit chubby (like a real queen bee, funnily enough), so she can also take a beating. Also, the crown on her head makes it clear that she is royalty which ties it all together, and later I decided it would be really funny if she threw it as her main attack, so she does.  

![A cool bee with two guns]({{ page.dir }}bee_gun.png)  
Finally, objectively the best bee, the bee with guns! (Where did he get those guns? Do they even make them that small? Also, does he even need sunglasses if he's a bee? Too many questions...) I love this dude because of how dumb the idea works, but a cool looking bee with guns makes it immediately clear that he will do DAMAGE, which is obviously reflected in the gameplay.  

One of the ideas I hope got across here is that switching over to bees that all look different helps make the gameplay more clear since how the bee looks helps inform what their role is, which makes the game much easier to pick up and follow. One similar benefit is that it frees me up to make their projectiles unique and readable as well, since a normal bee shooting its stringer will obviously look very different than a bee shooting bullets with a gun. They will need a lot less clarification, so I'll just list who shoots what before the pictures. shield bee - a glop of honey, normal and red bee - stringer, flower bee - nothing, queen bee - her crown, gun bee - bullets.

![The projectiles the bees shoot]({{ page.dir }}projectiles.png)  

After those touch ups and some other changes like making the hearts beehives, making an actual background, and changing the selection UI to be honeycomb-shaped, the last thing I needed to do was get the economy system working. I ended up going pretty simple by saying that every x time you get 1 honey and roughly balancing unit costs and strength around that, and that let to the fun idea of a having a timer represented as a flower growing petals to complete a full circle whenever the next honey is coming, who's sprites are shown below.  
![All 9 sprites the flower timer rotates through and the honeypot it gives you]({{ page.dir }}flower_timer_and_honeypot.png)    

The last touch was a name change, so I switched from Untitled Bug Game to just Bee Game to fit the new theming and keep it simple. All together, here's a look at what the game looked like after the changes:
![Gameplay of a late build featuring almost all of the game systems]({{ page.dir }}late_build_gameplay.gif)  

### The end

From the last update, the game was almost done. I had to touch up unity balancing a bit, get the honey/cost system actually implemented, making a title screen and instructions page, and finally a victory screen. Thankfully that final touch up didn't take too long since it most of it was small work that wasn't terrible but still fun. For some more visuals, here is the graphic on the instructions screen that I was pretty happy to throw together and then a gif of what the final game looks like.  

![The instructions seen in the game]({{ page.dir }}instructions.png)  
![The final version of the game]({{ page.dir }}final_build_gameplay.gif)  

---

### Closing thoughts and links  

So that's about it for Bee Game. A project with a lot of ups and downs that ended up as something that I'm really happy to have made. Part of that value to me comes from the fact that it's something I saw through from start to end with a mostly consistent vision all on my own, and it's even fun at the end. Even if now, a year after I finished Bee Game, I may be super rusty with Unity, but I still learned a lot of knowledge that I'll be able to brush off if I ever come back to it. On top of that, games are something that you can show off, which is why I'm able to write a long blog post like this one here after the fact which is also great. Also, I had no clue that I was actually good at making sprites for bees for a computer science student not terribly interested in art, which certainly helped bring me along while working on the project.  

Umm, buzz buzz?  
-Robert
