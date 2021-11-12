---
layout: page
title: Untitled Cupcake Game
permalink: /igda2
---

<body style="text-align: center">
<canvas id="unity-canvas" width=960 height=600 style="width: 960px; height: 600px; background: #231F20"></canvas>
<script src="assets/Build/Untitled Card Game.loader.js"></script>
<script>
  createUnityInstance(document.querySelector("#unity-canvas"), {
    dataUrl: "assets/Build/Untitled Card Game.data",
    frameworkUrl: "assets/Build/Untitled Card Game.framework.js",
    codeUrl: "assets/Build/Untitled Card Game.wasm",
    streamingAssetsUrl: "StreamingAssets",
    companyName: "DefaultCompany",
    productName: "Untitled Card Game",
    productVersion: "0.1",
    // matchWebGLToCanvasSize: false, // Uncomment this to separately control WebGL canvas render size and DOM element size.
    // devicePixelRatio: 1, // Uncomment this to override low DPI rendering on high DPI displays.
  });
</script>
</body>
