# TIledMazeGenerator
A maze generator for Tiles Map Editor (http://www.mapeditor.org/)

## Description
TIledMazeGenerator is a C++ executable program that create randomly generated, perfect maze for the Tile Map Editor. A perfect maze is descripted as one without any loops or closed circuits, and without any inaccessible areas. Also called a simply-connected Maze. From each point, there is exactly one path to any other point. The Maze has exactly one solution

## Features
 * Gapless Generation (No Clustered Mazes)
 * TMX Export (Creates a TMX File that is usuable immeadiatly)
 * Multi-Maze Generasion (Can create as many random mazes as you'd like)
 * GID Mapping (Maps tile sets to the maze)
 
## Config
The config file the generator will use is formatted in JSON (http://www.json.org/). Here's an example of what you JSON should look like:
```
{
    "tmx_name":"sample",                            /// TMX file name
    "tmx_layer":"sample_layer",                     /// TMX layer name
    "tmx_dimensions":25,                            /// Dimension of the maze (This must ALLOWS be an odd number)
    "tmx_dimensions_increment":2,                   /// Dimension size increase for preceeding mazes (Ex. mz1 = 25, mz2 = 27, mz-3 = 29) (Must be even number)
    "tmx_amount":5,                                 /// Amount of mazes to generate
    "tmx_tile_width":108,                           /// Width of an individual tile in your tileset
    "tmx_tile_height":108,                          /// Height of an individual tile in your tileset
    "tmx_tile_set":"../sets/sample_tile_set.png",   /// Location of the image
    "tmx_tile_set_name":"Sample Tile Set",          /// Name of the tile set in Tiled
    "tmx_gid_default":5                             /// Default tile to be used in your tile set
}
```

## How To Run
To run the generator, Use Command: `./TMXMazeGenerator -f {config file} -o {output directory)` 

## Binaries 
If you don't want to build the generator from source, you can find the binaries here:
The zip will containsa usage test and sample you can use

## Build
It's C++, Just import the code in any C++ compatable IDE, MAke sure you have C++11 flags set and build! But if you really lazy:

 * cmake - Open root directory containing `CMakeLists.txt`in shell

   mkdir build

   cd build

   cmake .. 

   cmake --build .
 * CLion - Open root directory containing `CMakeLists.txt`
 * Xcode - Coming Soon!
 * Visual Studio - Coming Soon!

## MIT Licence
```
MIT License

Copyright (c) 2017 Mozart Louis

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE
```
