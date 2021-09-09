---
title: Zelda 1 Demake
web_build_dir: "eecs_494_p1_zelda"
---

# {{ page.title }}

<center>
  <script src="{{ page.dir }}{{ page.web_build_dir }}/TemplateData/UnityProgress.js"></script>
  <script src="{{ page.dir }}{{ page.web_build_dir }}/Build/UnityLoader.js"></script>
  <script>
    var gameInstance = UnityLoader.instantiate("gameContainer", "{{ page.dir }}{{ page.web_build_dir }}/Build/{{ page.web_build_dir }}.json",{onProgress: UnityProgress});
  </script>
  <div class="webgl-content">
    <div id="gameContainer" style="width: 480px; height: 480px"></div>
  </div>
</center>

<br>


This is how you make a Unity game show up, just make sure the tag here is correct.

This is the play page. You would have an in-browser game available here (probably).

This is how you link an image here:
![This is how you link is an image]({{ page.dir }}preview.png)
