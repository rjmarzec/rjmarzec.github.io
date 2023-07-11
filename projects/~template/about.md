---
title: The Title Of The Project
type: (mobile/desktop app/game/tool)
tools: [engine/languages]
roles: [producer/programmer/artist]
release-date: 2000-01-01 # YYYY-MM-DD
description: "A short description of the project."
---

### {{ page.title }}

This is where basic text goes.  
End with 2 spaces for a newline!

<!--
  Include an embedded player for a Unity game like this.
  Remember to name the Unity export folder "WebGL" for this to work.
  Specify the window width and height by adding these tags above:  
    - unity-player-width: 894
    - unity-player-height: 495
-->
{% include projects/unity-web-build.html %}

<!--
  Include an embedded player for a YouTube video like this.
  Specify the video & window width and height by adding these tags above:  
    - youtube-video-id: LGWSEQF4kBg
-->
{% include projects/youtube-player.html %}

<!-- This is how you link an internal image/file and render it. -->  
![{{ page.assets }}/preview.png]({{ page.url }}/preview.png)

<!-- This is how you hyperlink to another page or downloadable file. -->
[External Link](https://itch.io/)  
[Internal Link]({{ page.url }}/play)  
[Click here to download]({{ page.url }}/stalwart-planet-guard-windows.zip)!
