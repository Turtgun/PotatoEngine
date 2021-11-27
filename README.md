# PotatoEngine

- README.md was copied from https://github.com/blurrypiano/littleVulkanEngine, their engine is way more mature, my engine is still being produced and SHOULD NOT BE USED as of now

### Install source files 

```
    git clone https://github.com/Turtgun/PotatoEngine
```

### Unix Build Instructions (Debian)
```
    sudo apt install vulkan-tools
    sudo apt install libvulkan-dev
    sudo apt install vulkan-validationlayers-dev spirv-tools
    sudo apt install libglfw3-dev
    sudo apt install libglm-dev
    sudo apt install cmake
```

### Unix Build Instructions (Arch)

```
    sudo pacman -S vulkan-tools spirv-tools cmake glm glfw
```

- Note glfw will install based on what window system you have, most notably glfw-wayland and glfw-x11


- To build, do
```
    cd PotatoEngine
    chmod +x unixBuild.sh
    ./unixBuild.sh
```

### MacOS Build Instructions

- [Download and install MacOS Vulkan sdk](https://vulkan.lunarg.com/)
  
- [Download and install Homebrew](https://brew.sh/)

- Then in a terminal window
  ```
    brew install cmake
    brew install glfw
    brew install glm
  ```
 
- To Build
   ```
    cd PotatoEngine
    ./unixBuild.sh
   ```

### Windows build instructions

- [Download and install Windows Vulkan sdk](https://vulkan.lunarg.com/)
- [Download and install Windows cmake x64 installer](https://cmake.org/download/)
  - Make sure to select "Add cmake to the system Path for all users" 
- [Download GLFW](https://www.glfw.org/download.html) (64-bit precompiled binary)
- [Download GLM](https://github.com/g-truc/glm/releases)
- Download and open the project and rename "envWindowsExample.cmake" to ".env.cmake"
- Update the filepath variables in .env.cmake to your installation locations

#### Building for Visual Studio 2019

- In windows powershell
  
 ```
  cd PotatoEngine
  mkdir build
  cmake -S . -B .\build\
  ```  
- If cmake finished successfully, it will create a LveEngine.sln file in the build directory that can be opened with visual studio. In visual studio right click the Shaders project -> build, to build the shaders. Right click the LveEngine project -> set as startup project. Change from debug to release, and then build and start without debugging.

#### Building for minGW

- [Download and install MinGW-w64](https://www.mingw-w64.org/downloads/), you probably want MingW-W64-builds/
- Make sure MinGW has been added to your Path
- Also set MINGW_PATH variable in the project's .env.cmake
- In windows powershell
  
 ```

  cd PotatoEngine
  ./mingwBuild.bat
  ```
- This will build the project to build/LveEngine.exe, double click in file explorer to open and run 
