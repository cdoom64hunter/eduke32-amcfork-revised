# Fork of EDuke32 for the AMC TC

This repository is a fork of the official eduke32 repository: https://voidpoint.io/terminx/eduke32 

It differs from the above by extending limits and altering hardcoded Duke3D features, specifically for the AMC TC. 

- The AMC TC can be found at: https://www.moddb.com/games/the-amc-tc

## Description
The primary purpose of this fork is to raise limits and alter hardcoded Duke 3D engine features to allow for greater flexibility 
in the development of the AMC TC, and to work around some bugs with legacy features which are difficult to resolve in CON code.

The changes are kept sparse to make merging with mainline eduke32 as smooth as possible.

Sidenote: The AMC TC makes extensive use of eduke32 modding features and will hence not be made compatible with Raze or GDX.

## Compiling from Source:

__Required packages:__
    
     * Basic dev environment (GCC >= 4.8, GNU make, etc)
     * SDL2 >= 2.0 (SDL >= 1.2.10 also supported with SDL_TARGET=1)
     * SDL2_mixer >= 2.0 (SDL_mixer >= 1.2.7 also supported with SDL_TARGET=1)
     * NASM (highly recommended for i686/32-bit compilation to speed up 8-bit classic software renderer)
     * libGL and libGLU (required for OpenGL renderers)
     * libgtk+ >= 2.8.0 (required for the startup window)
     * libvorbis >= 1.1.2 (libvorbisfile, libogg)
     * libvpx >= 0.9.0

To compile, simply run the command `make -j4` in the base folder.

Autodetection for Duke 3D is disabled, and the binary expects the `amctc.grpinfo` file, as well as the game data to be present in the same folder.

If you intend to experiment with the exe for non-AMC TC purposes, compile with the following parameter:

`make AMCTC=0`

__Additional build instructions can be found here:__

* Linux: <https://wiki.eduke32.com/wiki/Building_EDuke32_on_Linux>
* Windows: <https://wiki.eduke32.com/wiki/Building_EDuke32_on_Windows>
* MacOS: <https://wiki.eduke32.com/wiki/Building_EDuke32_on_macOS>

## Credits and Licenses

Fork created by Dino Bollinger.

* eduke32 is developed and maintained by Voidpoint LLC and is licensed under the GPL v2.0, see `gpl-2.0.txt`.  

* The Build Engine was created by Ken Silverman and is licensed under the BUILD license. See `source/build/buildlic.txt`. 

The AMC Team thanks the developers of eduke32 for their continued assistance and support over the past years.

**THIS SOFTWARE IS PROVIDED ''AS IS'' AND WITHOUT ANY EXPRESS OR
IMPLIED WARRANTIES, INCLUDING, WITHOUT LIMITATION, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.**
