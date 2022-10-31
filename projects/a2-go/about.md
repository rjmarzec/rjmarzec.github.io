---
title: A2-GO!
type: AR game
tools: [Unity]
roles: [Programmer]
release-date: 2022-10-31 # YYYY-MM-DD
description: "Tend to an ever-growing forest of trees while exploring the sights of Ann Arbor in this mobile AR experience! Just don't forget to fend off those pesky squirrels while you're here..."
---

### {{ page.title }}

<div style="text-align: center; padding: 0; border: 0; margin: 0;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/HEfQeH8ipTQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

A2-GO! is a reimagining of Pokémon GO as a educational & marketing tool for the city of Ann Arbor. In the game, users are tasked with tending to an ever-growing forest of trees that they build up by planting seeds as they walk around. Users are encouraged to check out local landmarks to unlock new types of trees, and the app gets them outside as trees grow based on how far users have walked around with the app open. They just have to watch out for those pesky squirrels - if a squirrel claims a tree as its own, it'll produce less leaves for the user to spend until they can shoo it away by tossing an acorn at it.

A2-GO! is the second large project from the first ever semester of UMich's VR & AR course. With the previous project being centered on VR and Unreal engine, this project was a bit different by focusing on AR and Unity. Once again, I worked with [Agatha Ta-Goetz](https://github.com/agathata) to put this project together over the course of 3 weeks. I'm a lot more experienced in Unity than I am Unreal Engine, so throughout this project I felt a lot more at home, and everything came together a lot smoothly. A lot of trouble this time around came from working with [Mapbox](https://www.mapbox.com/), an API for generating real-time maps in Unity (and other platforms) that was used to build to exploration part of the map. It was fun to play around with for the project, but only after some hiccups and dealing with surprisingly regular crashes that it brought with itself. In contrast, the AR side of things were pretty easy to interface with, though sometimes my phone had trouble finding the floor of my apartment while debugging. Could be worse I suppose. It was a bit of a journey from tech demo to playable game worth sharing, but I'm proud of the fact that the project managed to blossom into one that I could see being used in the real world - that really clicked for me when I had fun going out late at night to record the video embedded above.

---

### Significant features I implemented:
* Squirrel-fighting minigame
* Persistence across scenes
* Tree growth over time
* Orbit camera controls
* On-screen compass
* Landmark animations & info panels
