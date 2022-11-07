Importing objects from Blender to Unreal Engine:

I selected all the objects and selected .fbx option in export menu. 
Changed the path mode to copy and selected mesh only object types. Under geometry menu, I selected face option for the smoothing and exported the object in .fbx format. 
In unreal engine, I opened a blank template in games and disabled the started content and raytracing in the project defaults. 
Under file I created a new basic level. I deleted the ground level as it wasn't required. Then I imported the saved .fbx file. 
In the fbx import options, I checked Build Nanite Option and clicked import all. There were some warning messages, but as it doesn't affect my project, I ignored it and opened the content browser. 
From there I selected all the meshes and I dragged it into the scene. 
I added a new CineCameraActor. The filmback settings is 16:9 DSLR and changed the focus length to my requirement.

Animating the objects in Unreal Engine:

I have animated the objects in the sequencer. From the cinematics tab, I selected the add level seqeunce and created a new level sequence.
Then on the sequencer tab, I added the objects that I wanted to track. For that I clicked on the +Track button, then Actor to Sequencer and added the required objects.
To animate the object, I placed the cursor the on timeline from where i wanted to start the animation and clicked on the + symbol in the transform option to create a keyframe. Then I move the cursor to a new position and do the require positional changes to the object and then again keyframe that transform. This is how to entire animation in this video has been accomplished.
I also tracked the camera to increase the quality of the animation. In the similiar way as mentioned above, I tracked the CineCameraActor at various locations, to give that moving camera effect to the video.
After doing this, for each actor I clicked on the graph button on the Sequencer. This gives the graph of all the xyz transformation that I have done. From here is smoothed the curves to make the animation look much more smoother.

Rendering the Animation:

I decided to not use the rendering option that is available in the sequencer as it gives out inferior quality of video.
I turned on two plugins : Movie Render Queue and Movie Render Queue Additional Render Passes to render my animation.
Under Windows menu, Cinematics panel, I turned on the Movie Render Queue
In the Movie Render Queue panel, I added my sequence and then configured the settings.
In the settings panel , I changed the output option from .jpg sequence to .png sequence.
In the output settings, I changed to fps to 24 fps(film). 
From the add panel, I selected anti-aliasing. Set the temporal samples to 32 and turned on Override Anti Aliasing. And then I choose render local option.
The ouput came in 128 images. I converted these images into .mp4 video.
