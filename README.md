# OpenGL Rasterizer
This project is an OpenGL Rasterizer running through XCode on MacOS 13 Ventura.
Code is based on [LearnOpenGL](https://learnopengl.com/).
# Setup
The Xcode project is already configured, but here are my set up steps...
## GLFW
Use brew to install GLFW (inside a terminal): `brew install glfw`

> You can get a copy of brew if it's not on your machine [here.](https://brew.sh/)
## GLAD
Grab a copy from the [Glad Generator.](https://glad.dav1d.de/)
- Settings: 
	- API - gl - version: 4.3
	- Profile: Core
	- Generate
- Put a copy of the `glad` and `KHR` folders in `/usr/local/include`

## Xcode
1. Start a new command line C++ project
2. Build Settings > Header Search Paths > add `/opt/homebrew/Cellar/glfw/3.3.8/include` and ` /usr/local/include`
3. Build Settings > Code Signing Identity > Other > delete setting
4. Build Settings > *plus symbol* > Add User-defined Setting > `CODE_SIGNING_ALLOWED : NO`
5. 