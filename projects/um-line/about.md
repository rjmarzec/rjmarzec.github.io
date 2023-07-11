---
title: "''Um..., line?''"
type: desktop game
tools: [Unity, Adobe Illustrator]
roles: [Sole Developer]
release-date: 2023-07-09 # YYYY-MM-DD
description: "After years of having to sit through awful acting performances, it's finally time for you to take revenge. Become the heckler and ruin performances the way you know best: chucking tomatoes!"
---

### {{ page.title }}

<div style="text-align: center; padding: 0; border: 0; margin: 0;">
  <canvas id="unity-canvas" width=800 height=480 style="width: 800px; height: 480px; background: #231F20"></canvas>
  <script src="/projects/um-line/Build/WebGL.loader.js"></script>
  <script>
    createUnityInstance(document.querySelector("#unity-canvas"), {
      dataUrl: "/projects/um-line/Build/WebGL.data",
      frameworkUrl: "/projects/um-line/Build/WebGL.framework.js",
      codeUrl: "/projects/um-line/Build/WebGL.wasm",
      streamingAssetsUrl: "StreamingAssets",
      companyName: "rjmarzec Games",
      productName: "Um..., line - A game about heckling bad actors",
      productVersion: "1.0",
      // matchWebGLToCanvasSize: false, // Uncomment this to separately control WebGL canvas render size and DOM element size.
      // devicePixelRatio: 1, // Uncomment this to override low DPI rendering on high DPI displays.
    });
  </script>
</div>
<br>

> "A game about heckling bad actors."

While actors may take the role of heroes on stage, today, that is no longer the case. After years of having to put up with awful performances, you've decided to take your revenge against some of the worst thespians in the most devious way possible: chucking tomatoes at them until they get booed off stage!

The more performances you ruin, the stronger you'll be able to become. How many careers will you be able to destroy with your comically large slingshot at your side?

```
- CONTROLS -
Click, drag, and release: Launch tomato in aimed direction.
A/Left Arrow & D/Right Arrow: Reposition left or right, respectively.
```

![{{ page.assets }}/cover.png]({{ page.url }}/cover.png)

"Umm..., line?" is an action game that has you taking on the role of a theater heckler trying to get actors you dislike booed off stage. How? By chucking tomatoes until they turn bright red! (Just don't ask where you get all those tomatoes from...) Each performance you attend becomes increasingly more difficult to stop, but in-between rounds you've got a chance to make upgrades to help you keep pushing for an all-time high score. Give it a play above!

"Um..., line?" was developed over 48 hours as part of the GMTK Game Jam 2023, with this event's theme being "Roles Reversed". My first idea for game and the one I ended up running with was flipping the script on what you'd expect out of a game set in a theater. Rather than playing as an actor on stage and trying to not mess up, what we you were part of the audience trying to stir up chaos? From there the game grew into one about launching tomatoes from the back of the audience, and the rest was history. After wasting the first 24 hours being distracted and not getting much done, I really kicked it up a notch in the second half of the event to make something I'm proud of. I think the cartoony art style worked well for the silly concept, and early reviews seemed pretty positive. That said, the game did end up being more difficult than I intended on release and I couldn't upload a working WebGL build before submissions closed because of issues getting it loading properly (an issue I've been having with Unity for quite a while now, though I seem to have got it down for this blog at least). Still, I'm super happy with how nicely the final result turned out, so I'll call it another successful game jam under my belt.

---

Curious how development looked? Here's some progress milestone over the course of the event:

![progress-1.gif]({{ page.url }}/progress-1.gif)
*~12 hours in: Stage setup, moving actor, and tomato-launching system.*

![progress-2.gif]({{ page.url }}/progress-2.gif)
*~36 hours in: A working game flow with menus, and polished up core gameplay.*

![progress-3.gif]({{ page.url }}/progress-3.gif)
*Final product: Finished game with a bit more polish and extra bells & whistles.*

---

Download the standalone Windows build by click [here]({{ page.url }}/um-line-windows.zip)!

Don't forget to also check out the game's [itch.io page](https://rjmarzec.itch.io/um-line), [GMTK Game Jam 2023](https://itch.io/jam/gmtk-2023/rate/2160631), and [open source repo](https://github.com/rjmarzec/gmtk-game-jam-2023).

---

### Roles & Responsibilities:
* Everything! All code and assets were made by myself over the game jam's 48 hours, minus a few creative-commons sounds from [freesound.org](https://freesound.org/).
