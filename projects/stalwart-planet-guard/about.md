---
title: Stalwart Planet Guard
type: desktop game
tools: [Unity, Adobe Illustrator]
roles: [Sole Developer]
release-date: 2022-10-02 # YYYY-MM-DD
description: "Starworth is on a quest to build a new solar system, but pesky cats in UFOs keep getting in the way. Can you help this bright little star survive the attacks?"
---

### {{ page.title }}

<div style="text-align: center; padding: 0; border: 0; margin: 0;">
  <canvas id="unity-canvas" width=480 height=480 style="width: 480px; height: 480px; background: #231F20"></canvas>
  <script src="Build/WebGL_dev.loader.js"></script>
  <script>
    createUnityInstance(document.querySelector("#unity-canvas"), {
      dataUrl: "Build/WebGL_dev.data",
      frameworkUrl: "Build/WebGL_dev.framework.js",
      codeUrl: "Build/WebGL_dev.wasm",
      streamingAssetsUrl: "StreamingAssets",
      companyName: "rjmarzec Games",
      productName: "Stalwart Planet Guard",
      productVersion: "1.0",
      // matchWebGLToCanvasSize: false, // Uncomment this to separately control WebGL canvas render size and DOM element size.
      // devicePixelRatio: 1, // Uncomment this to override low DPI rendering on high DPI displays.
    });
  </script>
</div>

> The legends say that every 10 seconds, a new planet is born…
>
> … at least, so long as Starworth the Stalwart Planet Guard is around to make sure nobody interrupts.

Hop around the solar system while keeping those pesky UFO cats at bay! Every 10 seconds another planet spawns for you to hop around between, but so does another wave of cats.

Pick your upgrades wisely, and you might just be able to build out the largest solar system in the galaxy!

Beware: 1 bump from anything cat-related is all they need to take you down. How many planets can you make before you get bested?

```
- CONTROLS -
Left click: fire a star
Right click: jump to a different planet
```

---

Stalwart Planet Guard is an action game that has you balancing fending off endless waves of cats in UFOs while trying to manage the weird movement scheme of hopping between different planets in an ever-expanding solar system. At times you might be battling against gravity and yourself more than the cats, but when you're in the zone, flinging yourself around space while sniping off enemies has never been more satisfying. Feel free to give it a go in the web player above!

Stalwart Planet Guard was developed over 48 hours as part of the Ludum Dare 51 Compo (this event's theme being "Every 10 Seconds"), a more restrictive version of the traditional game jam format that gives you 24 less hours to work and requires you to build everything from scratch in a team of 1: code, art, and sound! Compared to my [last Ludum Dare project]({{ site.url }}/projects/wobbly-city-at-sea), this one was a much better experience. Everything came together pretty smoothly, and I ended the event with having pretty much all the features I was hoping to get into the game from the onset. There are a few rough edges I didn't get to smooth out and some balance issues (but who doesn't have those in their game jam project?), but the core gameplay loop is still satisfying. I've had the idea to work on a game that makes use of weird movement (shamelessly inspired by one of my favorite indie games, [Dandara](http://www.longhathouse.com/games/dandara/)), and this event was a good opportunity to do just that. It was nice to stretch the Unity muscle I hadn't made use of for a while, and in the end my reward was another title I'm proud to have put together.

---

This time around I took a few recordings of my progress throughout the event, so now I've got some development footage to share! Check out the gifs below.

![progress-1.gif]({{ page.url }}/progress-1.gif)
*A working planet spawning system and first pass on movement that would later be rebuilt.*

![progress-2.gif]({{ page.url }}/progress-2.gif)
*Fixed up movement (featuring being able to attach to planets) and a first sign of enemies in-game.*

![progress-3.gif]({{ page.url }}/progress-3.gif)
*A more complete build missing a few art assets and final polish.*

---

Download the standalone Windows build by click [here]({{ page.url }}/stalwart-planet-guard-windows.zip)!

Don't forget to also check out the game's [itch.io page](https://rjmarzec.itch.io/stalwart-planet-guard), [Ludum Dare 51 submission](https://ldjam.com/events/ludum-dare/51/stalwart-planet-guard), and [open source repo](https://github.com/rjmarzec/stalwart-planet-guard).

---

### Roles & Responsibilities:
* Everything! You can't compete in the Ludum Dare Compo unless you're working all on your own. :)  
