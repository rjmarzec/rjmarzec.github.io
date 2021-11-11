---
layout: page
title: Untitled Cupcake Game
permalink: /igda2
---

<html lang="en-us">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <title>Unity WebGL Player | Untitled Cupcake Game</title>
  </head>
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
</html>
