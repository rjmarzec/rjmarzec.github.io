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

Instructions:
* Movement: Arrow Keys  
* Sword attack: X  
* Special Weapons: Z  
* Rotate Special Weapon: Space  
* Custom Ice Wand: C  
* God Mode: 1  
* Custom Level Warp: 4  

Thanks for playing!
