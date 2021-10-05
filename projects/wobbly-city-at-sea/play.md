---
---

<body>
  <canvas id="unity-canvas" width=960 height=540 style="width: 960px; height: 540px; background: #231F20"></canvas>
  <script src="Build/WebGL.loader.js"></script>
  <script>
    createUnityInstance(document.querySelector("#unity-canvas"), {
      dataUrl: "Build/WebGL.data",
      frameworkUrl: "Build/WebGL.framework.js",
      codeUrl: "Build/WebGL.wasm",
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

Thanks for playing!
