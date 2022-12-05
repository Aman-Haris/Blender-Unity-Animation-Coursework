The models were exported in the .gltf format from the blender.
The libraries that were installed are glfw, glm, glad, KHR, stb and json packages.

Window Creation:
The window is created by initialising the glfw. The window size is defined to be 1920x1080.
"GLFWwindow* window = glfwCreateWindow(width, height, "CW3", NULL, NULL);"

Shaders:
A header file shaderClass.h is defined which is used to activate and deactivate the shader program.
A shaderClass.cpp file is porgrammed which builds the shader program and does necessary functions such as creating Vertex Shader Object, compiling the Vertex Shader into machine code etc.

Textures:
I have installed the open source library stb to import an image into the program so that I can convert it into a texture.
Texture.h header class has been created to bind,unbind or delete a texture.
Texture.cpp takes an image as input which is the converted into texture for the 3D model.
"glGenTextures(1, &ID);"

Camera:
A Camera.h header file is defined to store the vectors of the camera position, adjust the speed of the camera and it's sensitivity when looking around, handle camera inputs etc.
Camera.cpp program is programmed to initialise the camera and its position and add keystroke functions to create an exploring camera.
There are two types of keystroke movements added to the camera. One is using keyboard and other is using mouse.
The keyboard keystroke funtions are: W to move up, A to move left, S to move down, D to move right, Space to zoom out, Left Ctrl to zoom in, Holding Left Shift to increase spin speed, Releasing Left Shift to decrease spin speed.
The mouse keystroke functions are: Left mouse click to hide the mouse cursor, Right mouse click to show the mouse cursor. The mouse buttons can also rotate the model.

Lights:
A light.vert and light.frag files are defined to structure a light source.
The light source color is set to white. "glm::vec4 lightColor = glm::vec4(1.0f, 1.0f, 1.0f, 1.0f);"
A ambient lighting code is added to the default.frag to make the lighting even in the scence. 
Three types of lighting as been defined in the default.frag, they are: directLight(),spotLight() and pointLight().
We can choose which type of lighting we want by defining it in void main() class of the default.frag as shown below:
"void main()
{ // outputs final color
	FragColor = directLight(); }
  
Mesh:
A mesh class has been defined to gather all the necessary classes together to help in loading the model.
The heirarchy of the mesh class is: mesh: VAO, EBO, Camera Texture
                                          VBO       Shader
                                          
Mesh.h header file is created to initialize and draw a mesh.
Mesh.cpp program actually draws and activates the mesh by collecting all the necesary data such as vertices and positions.

Loading the model:

The models have been exported in the .gltf file format from the blender.
A json.h header file is created to parse json files as gltf format uses json file structure.
A Model.h header file is defined to load in a model from the file and to store its data.
A Model.cpp file is used to load and parse the model into json file structure.
The model is loaded using the code: "Model model("Models/Human.gltf");" which is coded in the Main.cpp file.

Reference:
"OpenGL Course - Create 3D and 2D Graphics With C++" by freeCodeCamp.org


  
  
  
  
  
