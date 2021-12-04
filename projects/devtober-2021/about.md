---
title: Devtober 2021
type: a month-long challenge
tools: Unity
roles: Sole Developer
release-date: 2021-11-01 # YYYY-MM-DD
description: "Devtober is a month all about working on projects just a little bit each day. Why is a cupcake fighting a meteor on an abandoned space ship? Come find out!"
---

### {{ page.title }}

Devtober is a personal challenge about working on anything development-related a bit every single day. Between participating in Ludum Dare 49 at the start of the month and a deckbuilder of sorts I put over the month, there's a lot I gone! Check out the blog posts below for a peak at what each day was like for me day-to-day, the postmortem for my thoughts over the month, or just check out the deckbuilder found right below!  

<body>
    <canvas id="unity-canvas" width=960 height=600 style="width: 960px; height: 600px; background: #231F20"></canvas>
    <script src="/projects/devtober-2021/assets/build/Untitled Card Game.loader.js"></script>
    <script>
      createUnityInstance(document.querySelector("#unity-canvas"), {
        dataUrl: "/projects/devtober-2021/assets/build/Untitled Card Game.data",
        frameworkUrl: "/projects/devtober-2021/assets/build/Untitled Card Game.framework.js",
        codeUrl: "/projects/devtober-2021/assets/build/Untitled Card Game.wasm",
        streamingAssetsUrl: "StreamingAssets",
        companyName: "rjmarzec Games",
        productName: "Untitled Cupcake Game",
        productVersion: "1.0",
        // matchWebGLToCanvasSize: false, // Uncomment this to separately control WebGL canvas render size and DOM element size.
        // devicePixelRatio: 1, // Uncomment this to override low DPI rendering on high DPI displays.
      });
    </script>

    <br>

    {% for post in site.pages reversed %}
        {% if post.path contains "projects/devtober-2021" %}
            {% unless post.path contains "about" %}
                <hr>
                {% assign post_date = post.path | split: '/' | last | replace: '.md', '' %}
                <h3>{{ post.title }}</h3>
                <div style="display:flex;justify-content:flex-end"><h6>({{ post_date }})</h6></div>
                <p>{{ post.content | markdownify }}</p>
            {% endunless %}
        {% endif %}
    {% endfor %}
</body>
