---
title: Toaster Story Postmortem
---

Hi there! Welcome to blog 2 of 3 about my work in the University of Michigan's game development course, EECS 494! After remaking the first dungeon of Zelda 1 with a partner last time, for this project we were let loose to build out our own cool ideas. I went for the exciting combination of a top-down shooting deckbuilder, and this blog will be a bit about the process to get there. If you're curious how a Toaster's Story plays into all of this, keep reading below!  

### The initial concept

So, how did we get here? Well, it all started off with a simple idea: top-down action games are fun because they can get very intense, and deck building games are super fun because well-planned strategies and a bit of luck can get you to start doing crazy things which is always the most fun. I had a huge list of games of inspiration in mind: Enter the Gungeon, One Step from Eden, Hearthstone, Teamfight Tactics, the Binding of Isaac, and Slay the Spire to name the most prominent ones. I thought games like Enter the Gungeon and the Binding of Isaac are great, but a lot of frustration in them can come from being dealt a bad hand to roll with and feeling like you lost because of it. Slay the Spire and Teamfight Tactics are both super engaging games because of the highs you can reach when everything goes just right alongside your good decision making, but given that there is little mechanical skill involved (it isn't hard to click the card I want out of my hand), their concepts potentially have some room to grow and spice things up there. From Hearthstone I took a strong liking to the way that they handle single-player drafting, letting you pick cards from weighted buckets that you think best align with your most powerful cards. Finally, One Step From Eden is what I think a  happy marriage of the concepts of fast-paced action mixed with deckbuilding looks like, so it had the strongest influence on the idea for my game as I was building it out. It's also a pretty underground game, so I would recommend checking it out if what you see here sounds fun!  

With a cool idea, all I needed was a nice theme. My long time playing League of Legends took me to Twisted Fate and Xayah as character to steal ideas from: Twisted Fate for the theme of throwing cards as a fun way to make use of the literal deck of cards you were building, and Xayah for her ability to recall feathers feeling super satisfying in game. Together I had a super cool gameplay loop: you played as some master of cards throwing out cards from a magical deck of cards to harm your foes, and to get your cards back you could just command them since they are all magical anyways.  

This sort of system offers a lot of flexibility in the ways you can get creative with effects in the game between special triggers on toss, recall, hit, recalled hit, or a wall hit causing all sorts of actions like speeding up your next attack, moving faster, making your next attack deal more damage, applying various statuses, dealing damage in an area, or having cards with modified base values to spice up an otherwise vanilla card. I was super pumped to get to work on an idea that has been stirring in my head for a while now, so a few days after finishing up that first class group project, I got to get to work!  

### The beginning  

Everything has to start somewhere, and for Toaster Story its with a very plain proof-of-concept. I needed a player who could move around, a deck of cards to throw, and then some way to actually throw cards in order to be able to actually do stuff in the game. I settled on just getting movement and card throwing working first, and with so few bells and whistles it really didn't take much to get it all going. From there figuring out how to get recalling working in the game also wasn't too hard, and then we had something that sort of played like a real game. Granted, it still doesn't look like one, but even messing around in this poor sandbox I knew that I was on to something.  

![Functional movement and card-throwing in a very simple environment]({{ page.dir }}working_concept_gameplay.gif)  

Next up: getting some more exciting cards functional and a way to edit your deck into something interesting. This part took me a bit to get right, since a lot was resting on the card system being flexible yet complete. After some thought I realized I could finally put inheritance to use in the first time in forever after being drilled on it being super important to learn in my classes. I still don't quite believe, but hey it worked out real well here so I guess I can't complain much.  

In heritance was able to work so nicely here because I need some sort of structure for a cards so that they could all be interfaced the same way while allowing for a wide array of effects. An example of this is that every card should know to come back to the player when the player wants to recall all their cards, but I shouldn't have to define that behavior for 10, 20, 50, 100, etc. cards individually, but putting that behavior in a class that every card extends off of means that the functionality always exists. From there, in each unique card I could override effects like what each card would do when it hits an enemy or a wall by only changing that 1 feature as everything else stays the same. It worked beautifully because it means that new cards could be built up with very little effort and get tossed into the game with no problem.  

After that I also needed a way for players to move around their deck, letting them swap in new cards and tossing ones they no longer needed. I didn't realize that Unity's UI system would be suffering to figure out how to work at first, so it all came together duct-taped on my first iteration through it. A big problem point I would run into down the line would be was the fact that I didn't have my UI scaling with screen size because I was unaware that it was an option! That meant that sometimes when you dragged your cards around and drop them somewhere they might miss the collision that you would think would happen. Still, it sort worked, and I was happy with that. Better yet, later I realized I could fix the issue by fixing the screen size, even though that isn't exactly ideal. I also gave up on proper practices and ended up hard-coding all the positions of cards that show up in your deck. It works, but it certainly isn't clean or scalable. The game ended up keeping this system since reworking it when I only had 2 weeks to build out the game meant it wasn't really worth it, but it's certainly something to look at again going forward.  

Anyways, at this point I have another gif of progress! This time with some nicer dummy placeholder pixel art, a "bounce card" that returns back to the player after hitting an enemy or a wall, and a very ugly first pass at a deck UI. Enjoy!  

![A working core of movement, throwing, unique cards, and deck editing!]({{ page.dir }}minimum_viable_product.gif)  

After getting that core functionality done, all I had left for my first assignment turn-in was to polish it up! I fixed the horrible colors, added some text instructions as you play, added a fast card that goes fast, added a ghost card that comes back very big, a gameplay loop with killing an endlessly spawning amount of scarecrows to kill that let you update your deck as you go. All together, I call this prototype "The Cardist," a nice way to communicate a game about a stick figure throwing cards in a stylistic way. Since this was an assignment turn-in, I've even got some download links below if the gif of some gameplay isn't quite enough for you.

[Download the Windows build here]({{ page.dir }}The_Cardist_Prototype_Windows.zip).  

[Download the Mac build here]({{ page.dir }}The_Cardist_Prototype_Mac.zip).  

![A polished version of the minimum viable product]({{ page.dir }}polished_minimum_viable_product.gif)  

### Round 2  

After that first hand-in, our class was tasked with fixing our games over the next week using info from a game-swap playtest session. Most of my feedback boiled down to "I don't know what's going on because there is nothing on the screen to tell me!" A very fair and accurate critique, given that I put no time into developing it out since I was just focused on getting that core gameplay done! This time however, I couldn't ignore it, so that was a big focus. On top of that, I wanted a game that was actually playable, so wanted to build out some levels, add a bunch of new enemies, and have a gameplay loop of winning or losing as you progress.  

Before getting to any of that, however, I was stumped. My pixel art from the first iteration only looked so good, so I new art style to tie everything together. I messed around in a sprite editor for a good our or so before realizing that something just wasn't clicking like it did for [Bee Game](https://rjmarzec.com/projects/Bee_Game) before this or something of the like. By some miracle, I opened up Adobe Illustrator to mess around, and then it happened: I drew a really cute toaster.  

![A neutral toaster]({{ page.dir }}toaster_normal.png) | ![An attacking toaster]({{ page.dir }}toaster_attacking.png)

*And he was beautiful.* I didn't think I had it in me to draw something so cute, but it all kind of took off from there since it just worked. I could have a fun toaster running around for some reason shooting out toast instead of cards at other food. I honestly still don't know why the toaster has the power to recall toast still, but when a crazy carrot runs at you I think it's the least of your concerns. Anyways, are all the enemies I put together and 3 of the more fun toasts:  

![An apple]({{ page.dir }}apple.png) | ![An orange]({{ page.dir }}orange.png) | ![A broccoli]({{ page.dir }}broccoli.png)  
![A pepper]({{ page.dir }}pepper.png) | ![A carrot]({{ page.dir }}carrot.png) | ![A scarecrow]({{ page.dir }}scarecrow.png)  
![Burnt toast]({{ page.dir }}toast_burnt.png) | ![Jelly toast]({{ page.dir }}toast_jelly.png) | ![Egg toast]({{ page.dir }}toast_egg.png)  

With the new artwork done, I got it set up which let me start work on getting enemies set up! I started out with an apple as a base, and the rest were just tweaking numbers on the different properties and swapping out some sprites which was real nice. I took some inspiration from Enter the Gungeon here with slow-moving red pellets that stack up nicely to make a game focused around careful dodging, which ended up feeling pretty good when things get intense with multiple enemies. Anyways, I'm getting a bit sidetracked. Below is what that first enemy looked like, even wobbling to add some extra feel of movement.

![The first working enemy, an apple]({{ page.dir }}apple_enemy.gif)  

With that done, it was back to some more boring stuff: throwing together more levels, putting together duct-tape solution UI for showing players their next toasts, batteries displayed as health, and fixing up the deck swap UI. On the deck swap touch up in particular I started to get a better understanding of how the Unity UI system works, but I'm still not the biggest fan... I at least fixed the scaling problem, and then I redid the graphics to make it much clearer what you are supposed to do on that screen. On a related note, I also got to suffer through getting a pop-up description for cards on mouse hover working, which again helped that clarity. Sure, you might that the cards were doing something different, but what exactly are they doing? That question came up a lot in playtesting, so this hopefully addresses it, although while being a bit wordy.  

Another big part of the game that really breathed a lot of life into it was visual changes on hit and sound! A simple red flash did a nice job, and then you've got sounds for anything getting hit and pickups to keep the game from being a plain mess. On the note of sounds, I'll bring up the fact that none of them are my own! A big thanks to [FreeSound.org](https://freesound.org/) here for being an open website for free user-generated sounds. If you're curious to listen what I used in game, [click here]({{ page.dir }}Toaster_Story_Sound_Credits.zip) for the credits on where I got what to use when.  

From there, I had a bit of bug catching to finish up, some balancing tweaks, and then I was all done. The end result was the game you can play all the way at the top of this page (if you haven't yet, now is a pretty good time to try it out!), but look below if you just want to see a short gif of what the final gameplay looked like!  

![Gameplay from Toaster Story's final build]({{ page.dir }}final_build_gameplay.gif)

### Robert's Quest (and his reflection on the game)  

Even if this project was pretty stressful with how long it took to put together, I'm really happy with how it all turned out. The art and sound really pulled together a really cool concept into one nice bundle to make a super engaging single-player experience. On that front I think I really pushed past my own expectations on where this would all end up, beating out the [Bee Game](https://rjmarzec.com/projects/Bee_Game) in quality when I put that one together over the course of 1 semester instead of 2 weeks. I definitely could have done better on being more consistent with good practices, but you have to start making something dirty before you learn to make it clean, so I'm alright on that front now that I'm stopping the game here for now.  

One bittersweet note is that over time I feel like the game lost a bit of the original touch that made it interesting. At the point it is now, the game really revolves around shoving any cards into your deck that you can find, and only getting creative once you have filled up your maximum of 24 slots for toasts. I think this is really in part due to the fact that there aren't enough new toast pickups to allow you to start making engaging decisions, there aren't any penalties for reloading so endless shooting of anything becomes the best option, and I didn't have the time to implement some sort of "artifact" system that could have put a lot of emphasis onto focusing your deck around 1 style of play or type of card. There's certainly a lot to work with here so I don't think I'll be done with Toaster Story for good. For now, yes, but will I return in the future? I think I very well might. Out of everything I'm just happiest knowing I can draw some pretty cute and vibrant art that will probably be my game style going forward which should be a lot of fun.  

If you got this far, thanks as always! This write-up certainly was a lot of work to write, but I hope you might have gotten something interesting, even if it's just a picture of a cartoon-style carrot that is yelling for some reason. Speaking of which, check the link below for all my original game assets all zipped together, Adobe Illustrator file included as well if you're interested to look inside.  

[Download Toaster Story's assets]({{ page.dir }}Toaster_Story_Assets.zip).  

Thanks again for reading, playing, and having a good time,  
-Robert
