# [Kaleidospace](https://github.com/natronics/kaleidospace/)

_November 2017_

I was thinking about two things recently. First: some of the many [really cool timelapse videos of Earth from the International Space Station](https://www.youtube.com/watch?v=FG0fTKAqZ5g), and second: abstract generative art.

The colors and movement reminds me of a [kaleidoscope](https://en.wikipedia.org/wiki/Kaleidoscope). I wondered what it would look like if I used a space time-lapse video as the input for a kaleidoscope. A kind of abstract view of Earth from space. I was thinking about how I might go about this and I decided I could "build" a virtual kaleidoscope as a simple scene in the 3D animation tool [Blender](https://www.blender.org/). Then I could render an animation as my output video.

I downloaded one of the recent really nice time-lapses from <https://eol.jsc.nasa.gov/BeyondThePhotography/CrewEarthObservationsVideos/>. Then I created an empty blender layout with the camera pointed at a screen-shaped rectangular mesh. I mapped a test image to this mesh as a texture and then made three identical tall skinny meshes 120&deg; apart between the camera object and the screen mesh. Then I set the material to be a perfect mirror and hit render!

![Output of a random frame from the first try from Blender](docs/images/first_try_still.jpeg)

It worked out pretty great! I was really pleased with the output. With a still image it was really boring of course since nothing moved. I knew a video would be better, but I still wanted to add some extra movement to the final result. So I used the animation keyframes in Blender to set the kaleidoscope to slowly rotate. This should make the alignment of the kaleidoscope effect slowly shift even as the video plays underneath it. I also added a couple compositing effects so the output isn't perfect (barrel distortion and some dispersion).

Video:
------

<https://vimeo.com/242401422>


Working with Blender
--------------------

There are two .blend files. `studio.blend` is the first test image that I played around with. `kaleidospace.blend` is the final render version with a video mapped as the base mesh texture.

I didn't include the source video in this repo because of the size. However if you download any video then open the blender file and select the mesh named `Image`. Then go to the Texture tab in the properties view and there will be one Texture loaded. Under the `Image` section is a place to set the file to import. Select the video file you downloaded.

Note that sometimes Blender fails to import move frame metadata correctly. If you get a blank texture try setting the start frame to 1 and the offset to 0 (in the frame settings just below the file import section).

Try switching to Animation view and play with the z-rotation animation curves. Or select the camera and in the camera properties change the focal length to make the kaleidoscope zoom in and out. 
