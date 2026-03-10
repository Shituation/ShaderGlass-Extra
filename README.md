## ShaderGlass-EXTRA (FORK)

Overlay for running GPU shaders on top of Windows desktop.
This fork adds saving the size of the shader window and its position on profiles, so you can now create profiles for different apps with different sizes and window positions and restore them automatically when loading the profile.

### Features

* applies shader effects on top of desktop, in a floating window or full-screen
* built-in [RetroArch](https://github.com/libretro/RetroArch) shader library (1200+ shaders!) covering:
  * CRT monitor simulation
  * image upscaling
  * TV, VHS and handheld simulation
  * softening, denoising, blur, sharpen and many more
  * you can even use it on top of YouTube, Twitch or modern games
  * allows capture from a USB source (webcam or capture card)
  * saving and loading profiles
  * import of external .slangp/.slang shaders
  * high customizability with various options, operating modes and shader parameters
  * can be captured by OBS (using Game Capture source)

Check out [Online Manual](https://mausimus.github.io/ShaderGlass/MANUAL.html)

<br/>

### Requirements

* __Windows 10, version 2004__ (build 19041) or __Windows 11__
  * will work on version 1903 but in limited capacity (no Desktop Glass mode)
  * Windows 11 allows the __removal of yellow border__ (see [FAQ](FAQ.md#windows-10) for tips on avoiding it on Windows 10)
* DirectX 11-capable GPU

<br/>

### Demo

Click to view on YouTube

[![ShaderGlass (YouTube)](https://img.youtube.com/vi/gWOcucS9_mg/maxresdefault.jpg)](https://www.youtube.com/watch?v=gWOcucS9_mg)

<br/>

### Code

Built using Visual Studio 2022 using ISO C++ 20, Windows SDK 10.0.26100, Windows Capture API and DirectX 11.

ShaderGlass includes a limited implementation of RetroArch shader back-end using DirectX 11.
[ShaderGen](ShaderGen) is a command-line tool for converting Slang shaders 
into .h files which can be precompiled in ShaderGlass. The conversion process relies on:
1. [glslang](https://github.com/KhronosGroup/glslang) for converting Slang/GLSL shaders to SPIR-V
2. [SPIR-V cross-compiler](https://github.com/KhronosGroup/SPIRV-Cross) for converting those to HLSL (DX11 format)
3. [Direct3D Shader Compiler (fxc.exe)](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk/) for pre-compiling into bytecode

<br/>

### Notices

* ShaderGlass application is provided under [GNU General Public License v3.0](LICENSE)

* Includes precompiled shaders from [libretro/RetroArch shader repository](https://github.com/libretro/slang-shaders).
Please refer to copyright notes within shader code for detailed copyright and license information about each shader.

* App icon courtesy of Icons-Land

* Big kudos to RetroArch team, emulator developers and the wide retro community!

* Thanks to @mausimus for his permission to fork his app.

