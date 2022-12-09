---
title: vrEnable
type: VR empathy training experience
tools: [Unreal Engine]
roles: [Programmer]
release-date: 2022-12-08 # YYYY-MM-DD
description: "Explore a surrealist view of UMich's Beyster 1695 computer lab in the world of VR! Be sure to speak with the locals, print an apple or two, and maybe even go play a round of beer pong in the back."
featured: true
---

### {{ page.title }}

<div style="text-align: center; padding: 0; border: 0; margin: 0;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/dOHusIkNf1Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<h1>
  <p style="text-align: center;">
      <a href="https://megalodon-oleander-nnd9.squarespace.com/">Check out the project website here!</a>
  </p>
</h1>
<h3>
  <p style="text-align: center;">
      (password: vrenable)
  </p>
</h3>

vrEnable is a corporate empathy training tool designed to help your workers better understand what life is like for their impaired teammates by putting them through a day in their eyes. While many empathy training experiences exist, none quite fully capture or convey what the experience is like from the first person. By bringing these experiences into the world of VR, vrEnable seeks to better bridge the gap in understanding between coworkers with its world-class empathy training modules. Currently, vrEnable's main experience focus on demonstrating what life in an office space can look like for people with attention-deficit/hyperactivity disorder (ADHD).

vrEnable was the final project for the first semester of EECS 498, UMich's VR/AR course. This time working in groups of 4/5, teams were tasked with building out a prototype for a tech product involving AR/VR over ~4.5 weeks. For this project, I teamed up with [Agatha Ta-Goetz](https://github.com/agathata), [Ayman Said](https://github.com/flaymien), [Jonathan Lin](https://github.com/linjonathan2001), and [Zareef Safdar](https://github.com/safdarzareef) to build an empathy training app in VR because we found the tech interesting, the problem personal, and current products lacking. This time with some more Unreal Engine experience under our belts, things went a lot smoother than our first projects, but there were still lots of fun challenges to solve along the way, especially when so many hands were involved in the making of the app. vrEnable's ADHD simulator was what we primarily worked on for the product side of things, which is a simulation specifically trying to emulate how a person is ADHD often has trouble sticking to completing individual office tasks when they constantly have competing thoughts, productive or otherwise. If that all sounds interesting, you can check out some of the demo footage from week 1 [here](https://youtu.be/x3cbPt-XDeo), and week 2 [here](https://youtu.be/G676XEbt8-s).

Originally, our team actually wanted to put together a 3D modeling tool in VR aimed at students wanting to take notes in a 3D space, since some studies like architecture or chemistry require translating 2D models to 3D ideas in a way that can be difficult to first grasp. We named the project "CubeNotes", and you can find some early demos of it [here](https://youtu.be/hVo4zZZo3bs) and [here](https://youtu.be/SVOyyp76yc4). While we were happy to keep going with our product, found ~2 weeks into our development cycle that Google had already done it better with [Google Blocks](https://arvr.google.com/blocks/), so the team ultimately made a super late 180-degree pivot into what eventually became vrEnable. In some sense we ended up with 2 projects for the price of 1, though I would have loved to have seen either a bit more polished with the 2 weeks the other ate up. That's all to say that this whole experience was a lot of fun, even if it was a bit stressful and busy at times along the way.

---

### Significant features I implemented:
* Non-teleporting movement scheme
* VR pen tool (CubeNotes)
* Note save system (CubeNotes)
* Snap-positioning for grabbable objects
* Sound system
* Lots of small fixes, bugs, and merge conflicts
* All basic task behaviors, including:
* - Making coffee
* - Printing & delivering a meeting agenda
* - Talking to your boss
* - Eating a sandwich
* - Sending an email

---

[Check out the project on GitHub here!](https://github.com/rjmarzec/vrEnable)
