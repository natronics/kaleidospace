---
layout: article
title: Kaleidospace
---

# Kaleidospace

<span class="pubdate">November 2017</span>

 I was thinking about two things recently. First: some of the many [really cool timelapse videos of Earth from the International Space Station](https://www.youtube.com/watch?v=FG0fTKAqZ5g), and second: abstract generative art.

The colors and movement reminds me of a [kaleidoscope](https://en.wikipedia.org/wiki/Kaleidoscope). I wondered what it would look like if I used a space time-lapse video as the input for a kaleidoscope. A kind of abstract view of Earth from space. I was thinking about how I might go about this and I decided I could "build" a virtual kaleidoscope as a simple scene in the 3D animation tool [Blender](https://www.blender.org/). Then I could render an animation as my output video.







I downloaded one of the recent really nice time-lapses from <https://eol.jsc.nasa.gov/BeyondThePhotography/CrewEarthObservationsVideos/>. Then I created an empty blender layout with the camera pointed at a screen-shaped rectangular mesh. I mapped a test image to this mesh as a texture and then made three identical tall skinny meshes 120&deg; apart between the camera object and the screen mesh. Then I set the material to be a perfect mirror and hit render!

<div class="columns">
  <div class="column">
    <a href="images/blender_setup.png">
      <img class="img-responsive" src="images/blender_setup.png" alt="Setup of the virtual kaleidoscope in Blender">
    </a>
    <p>Setup of the virtual kaleidoscope in Blender</p>
  </div>
  <div class="column">
    <a href="images/first_try_still.jpeg">
      <img class="img-responsive" src="images/first_try_still.jpeg" alt="Output of a random frame from the first try from Blender">
    </a>
    <p>Output of a random frame from the first try from Blender</p>
  </div>
</div>


It worked out pretty great! I was really pleased with the output. With a still image it was really boring of course since nothing moved. I knew a video would be better, but I still wanted to add some extra movement to the final result. So I used the animation keyframes in Blender to set the kaleidoscope to slowly rotate. This should make the alignment of the kaleidoscope effect slowly shift even as the video plays underneath it. I also added a couple compositing effects so the output isn't perfect (barrel distortion and some dispersion).

Output
------

vid goes here

You can download the basic blender file I made here:

 - [blend]()

This article and blender files are all in a git repository. You can clone the entire thing:

 - [github]()
