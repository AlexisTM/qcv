QCV v00.60
============

Fork from http://sourceforge.net/projects/qcv/?source=directory

This Fork would link it to ROS. (Robotic Operating System)

Read qcv-code/README.txt and qcv-mods/README.txt

Note: increment the number of horizontal and vertical screens in the main visualization widget to view all screens.

Introduction
----------

QCV is a Qt-based computer vision framework library that provides an easy to use interface to display, analyze and run computer vision algorithms. The library is provided with practical examples to show what you can do with just a few lines of code. OpenCV is used as the supporting computer vision library.

QCV provides interfaces for C and C++. The C interface is a set of simple function calls to allow the user to visualize data and obtain events from the system and user input. 

The C++ interface has more features allowing the user to run and analyze complex computer vision algorithm in a few lines of code (see the stereo and surf examples).

QCV offers a 2D visualization tool, an on-line on-the-fly parameter editor, a clock tool to evaluate computation times, and a control tool to manipulate input video and sequences of images.

Multiple application examples that demonstrate the main features of this framework are provided in the last release.


Features
----------

* Computer vision toolbox including
* Powerfull 2D visualization tool
* 3D data visualization
* On-the-fly parameter editor
* Image sequence playback control tool
* Clock handling
* C and C++ interfaces
* Application examples to show easy of use
* Clear and intuitive programming style

qcv-code
-----------

To install the source code you will need to install first 
OpenCV 2.X and Qt 4.X. You will also need OpenGL and glut.
To obtain the code from SourceForge.net you need mercurial
as well. CMake and g++ are required to compile the code.

If you run Ubuntu 10.x or 11.x, these lines should provide
you with the required dependencies:

```bash
sudo apt-get install freeglut3-dev mercurial libqt4-dev cmake g++
sudo add-apt-repository ppa:gijzelaar/opencv2
sudo apt-get update
sudo apt-get install opencv
sudo apt-get install libopencv-dev
```

If you want 3D display capability, you will need to install
QGLViewer

```bash
sudo apt-get install libqglviewer-qt4-dev
```

If you run another Ubuntu version (including 12.x) or
another Linux distribution, you will need to download 
OpenCV and install it in your system.

Now, get the code now from SourceForge.net

```bash
git clone http://github.com/AlexisTM/qcv
```

or download the tar.gz (tar.bz2 or zip) file from here: http://sourceforge.net/projects/qcv/?source=directory

To compile the code, cd to the source code directory:

```bash
cd qcv
mkdir build
cd build
cmake .. -DCMAKE_INSTALL_PREFIX=$HOME/local
make
cd $HOME/qcv/build/bin # Bin directory 
```

### C examples (qcv core only)
```bash
./helloWorld
./toyClockExample
./checkStereoPair imgs/left.pgm imgs/right.pgm
./sobelExample imgs/seq/*c0*.jpg
./imgViewer --cam imgs/seq/*c0*.jpg --cam imgs/seq/*c1*.jpg
./anaglyphStereo --left imgs/seq/*c0*.jpg --right imgs/seq/*c1*.jpg
```

### C++ examples (operators, editor and sequencer)
```bash
./stereoExample
./imgScalerExample somevideo.mpg
./sobelExample2 somevideo.mpg
./surfExample sequence.xml
./houghTransformExample sequence.xml
```

You will need to provide valid videos as parameters,
(or just use the provided image sequence by using
"sequence.xml" instead).

Plase, send comments or questions to hernan.badino@gmail.com

qcv-mods
-----------

Copyright (C) 2015 Hernan Badino <hernan.badino@gmail.com>

This file is part of StereoSFM

StereoSFM is under the terms of the GNU General Public License v2.
See the GNU GPL version 2.0 for details.
StereoSFM uses dual licensing. Contact the author to get information
for a commercial/proprietary license.

StereoSFM is distributed "AS IS" without ANY WARRANTY, without even 
the implied warranty of merchantability or fitness for a particular
purpose.

In no event shall the authors or contributors be liable
for any direct, indirect, incidental, special, exemplary, or
consequential damages arising in any way out of the use of this
software.

By downloading, copying, installing or using the software you agree
to this license. Do not download, install, copy or use the
software, if you do not agree to this license.

### Instruction

```bash

cd qcv-code
mkdir build
cd build
cmake ..
make
```bash

then

```bash
cd qcv-mods
mkdir build
cd build
cmake ..
make
```

Binaries and a copy of the parameter files for qcv-mods will be placed in qcv-mods/build/bin
