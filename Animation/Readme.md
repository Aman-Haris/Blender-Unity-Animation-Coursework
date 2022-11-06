Importing objects from Blender to Unreal Engine:

I selected all the objects and selected .fbx option in export menu. 
Changed the path mode to copy and selected mesh only object types. Under geometry menu, I selected face option for the smoothing and exported the object in .fbx format. 
In unreal engine, I opened a blank template in games and disabled the started content and raytracing in the project defaults. 
Under file I created a new basic level. I deleted the ground level as it wasn't required. Then I imported the saved .fbx file. 
In the fbx import options, I checked Build Nanite Option and clicked import all. There were some warning messages, but as it doesn't affect my project, I ignored it and opened the content browser. 
From there I selected all the meshes and I dragged it into the scene. 
I added a new CineCameraActor. The filmback settings is 16:9 DSLR and changed the focus length to my requirement.

Animating the objects in Unreal Engine:

