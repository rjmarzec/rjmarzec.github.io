---
layout: page
title: A Wobbly City At Sea
permalink: /igda1
---

<body>
  <canvas id="unity-canvas" width=960 height=540 style="width: 960px; height: 540px; background: #231F20"></canvas>
  <script src="projects/wobbly-city-at-sea/Build/WebGL.loader.js"></script>
  <script>
    createUnityInstance(document.querySelector("#unity-canvas"), {
      dataUrl: "projects/wobbly-city-at-sea/Build/WebGL.data",
      frameworkUrl: "projects/wobbly-city-at-sea/Build/WebGL.framework.js",
      codeUrl: "projects/wobbly-city-at-sea/Build/WebGL.wasm",
      streamingAssetsUrl: "StreamingAssets",
      companyName: "rjmarzec Games",
      productName: "Wobbly City At Sea",
      productVersion: "1.0",
      // matchWebGLToCanvasSize: false, // Uncomment this to separately control WebGL canvas render size and DOM element size.
      // devicePixelRatio: 1, // Uncomment this to override low DPI rendering on high DPI displays.
    });
  </script>
</body>

Interested in hearing more about the game? Check out the [itch.io page](https://rjmarzec.itch.io/wobbly-city-at-sea) or the [original Ludum Dare 49 submission](https://ldjam.com/events/ludum-dare/49/wobbly-city-at-sea).
