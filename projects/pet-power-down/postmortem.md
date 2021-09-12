---
title: Pet Power Down Postmortem
---

Hi there! Today I'll be writing about my time putting together Pet Power Down, a computer game designed around answering a complicated question: How do we design games for the visually impaired? Keep reading for a look at what that question meant to my team and what we made along the way.  

### Some background and the initial idea

Before all the good stuff, let's talk a bit out why the game came to be. In my first semester of Freshman year at university, I signed up for a class named "Gaming for the Greater Good," a course where students would get into groups of 4 to put a game together over the semester using GameMaker Studio 2. Each semester, the class would focus on a specific disability to have the games catered towards, and this semester the focus was on visual impairments, or people who have reduced, little, or no ability to see.  

From a game design standpoint I found the problem super interesting. It's hard to think of any game that doesn't use the screen it displays to transmit it's vital information, and working around that issue is a fun one. The idea I ended up settling on was abandoning visuals altogether! After all, if you don't have any visuals you need to look at to play the game, then there shouldn't be any meaningful difference between playing with and without working vison. It's the dumb yet genius type of approach.  

From there the idea that came to me was having to search out something in the dark that made noise back at you so that you could echolocate them. I had some trouble figuring out what theming would work for that, but eventually I settled on the idea of searching for pets in the dark after a power outage (hence the name Pet Power Down). I figured it worked on multiple fronts: it's dark because the power is out, you're searching for pets because you are in your home, and your pets are making sounds because that's what animals do.  

Every student in the class had to put a similar pitch together like I did, and mine was one of the ones that survived the culling and made it to live pitches where I picked up some teammates to make a team of 4. Development got started from there, with me taking the role of one of the two main developers, with a focus on movement, controls, and level design. With that background out of the way, let's go into the game!  

### Early concept  

Part of the project proposal phase in the class involved writing up a document including some mock-up sketches of how our games were supposed to work, and I think they fit real nice here to help illustrate what the game is actually like if my previous description didn't do a great job. Here's an overview of some of my concept sketches:  

![A concept sketch of what a room with perfect vision looks like]({{ page.dir }}concept_level_start.png)  

Here's a look at what the start of a level looks like with perfect vision. You have your player at one side of the room and some sort of pet on the other. The room you're in can take up forms of all sorts of different twists and turns and it's split up into a grid.

![A concept sketch of the dark room the player sees]({{ page.dir }}concept_level_dark.png)  

Of course, that last sketch misses the whole point of the game: not needing to see. While under the hood levels would look like the last picture, the players would see some something to the effect of the above. You are able to see your player character, some parts of the room are darkened so you don't see everything (you'll see this later), and the only pointer you have towards the animals you are looking for is the sounds they make that you hear coming from their direction.

![A concept sketch of moving in a row]({{ page.dir }}concept_level_movement.png)  

And here we have a showcase of what the core gameplay loop looks like. Each "turn" the player is able to make some number of movement in any of 4 directions along the grid of the map. After the player makes their movement, the pet will make their movements following a similar set of rules and unique movement patterns based on the animal. After that, the pet will make a noise back at the player so that they can readjust their strategy and next steps before repeating the process.  

All that together, we have ourselves a game! After a few months of effort between a team of 4, we were able to fully flesh out the game into something playable. At this point I would go into more about what my role was on the team, but my memory on exact details is shaky since the completion of the project predates this post/website by a year and since we used Google Drive as our form of version control I can't go back and easily verify either. I'll note again that my roles were movement controls for the players, basic AI for the pets in the game, and level design. What I have to show instead are some pictures of what the final game looked like in different levels, so enjoy those to follow.  

### The finished game  

Now for the exciting stuff: screenshots of the finished game! Showing off all 24 levels here would be a lot, so I'll just show the first couple few and then some other interesting ones. Before I get into that, here some clarification on the parts of each level: the girl is the character the person controls, the pet-looking things are the pets that player has to catch, the red squares and furniture are walls the player cannot pass (and that make a bumping sound when you try to walk onto them), the green and blue squares are carpet the player can walk on, and the black parts of the map are... uh... the void? As for how the void fits into a simple game like this, don't ask.  

![Level 3]({{ page.dir }}level_3.png)
![Level 3, but dark as seen in game]({{ page.dir }}level_3_dark.png)

Let's jump ahead to level 3 first to show off what the darkness in the game looks like. It turns out that the game feels terrible if you can't see *anything*, so the best balance between seeing everything and seeing nothing came out to be the flashlight effect shown above. Having the flashlight means that you don't get frustrated bumping around in the dark while still making navigating require echolocation on the larger scale. The other picture above is the room with the flashlight taken off, just for clarity here and now what it would normally look like.

![Level 1]({{ page.dir }}level_1.png)
![Level 2]({{ page.dir }}level_2.png)

Here's level 1 and 2. Both are super simple to get players warmed up to the controls and what they are looking at and how to move. One more unique feature of these two level is that they both have the darkness off to begin. It doesn't make sense to throw players into the darkness from the start, so for the first two levels the players get some help there.  

![Level 4]({{ page.dir }}level_4.png)
![Level 5]({{ page.dir }}level_5.png)
![Level 6]({{ page.dir }}level_6.png)

Here's levels 4, 5, and 6. They mix things up with more interesting layouts and even multiple pets. Nothing too crazy here, but a start to more varied levels.  

![Level 9]({{ page.dir }}level_9.png)
![Level 10]({{ page.dir }}level_10.png)
![Level 21]({{ page.dir }}level_21.png)

Levels 9, 10, and 21. I'm pointing out these levels since I liked they way they lead players: although the rooms were complex and might confuse players if they had to go from start to end in one go, pets were put in specific places to guide players down the right path as they pick up pets along the way.  

![Level 11]({{ page.dir }}level_11.png)
![Level 16]({{ page.dir }}level_16.png)
![Level 20]({{ page.dir }}level_20.png)  

Levels 11, 16, and 20. While the last 3 levels were examples of levels that worked well, I think these ended up being pretty poor. In these the pets are hidden behind walls or obstacles, so when the players walk in their direction, they end up getting stuck without a clear path to progression without some trial and error testing, which is terrible.  

That's only 1/2 of the levels shown here, so I'll leave the rest for you to check out in the game if you care. See below for that the link to that.  

### Wrap up  

So how well did Pet Power Down work as a game for the visually impaired? It turns out, pretty bad. While the concept was good on paper, the game is unplayable completely in the dark since it's really hard to build a map out of complicated rooms unless there was some audio cue way to get a full picture of the room through sounds. Since everything was lacking a lot of polish too (inconsistent visual style, large sound drop offs, long pet sound durations that would overlap, clunky movement, poor level design, etc.), the experience ended up getting bogged down in more than 1 way, which lead to an experience that was interesting to try but not so much to play. Ironically, because out the flashlight effect blocking out a large chunk of what people could see and having a shaded area around the player, people with visual impairments could have a harder time parsing the visual information necessary for playing the game. Which is bad. If the players that you tried to cater towards have the hardest time playing the game, you messed up.  

Sure, the game wasn't perfect, but putting something unique together with friends was a lot of fun. It's also one the first well put together projects I've worked on worth showing, which is why I'm writing about it here. Messing up is part of the process, and it just means that maybe I think through my projects more in the future and try to figure out how something will go wrong before it does.  

If you've gotten this far, thanks for reading through a write-up of Pet Power Down! I hoped you took something out of exploring an interesting idea through my eyes as it got shaped into it, and hopefully you enjoyed a bit of the game if you tried it out as well. This was also my first project blog post on this site, so yay me for that as well, and here's to many more with hopefully a more defined writing style from here on out. That's all for now, so thanks again for stopping by.  
-Robert
