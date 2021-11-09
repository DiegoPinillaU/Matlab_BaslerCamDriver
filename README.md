## Fork of Matlab_BaslerCamDriver
I've refurbished the original code in order to communicate with a Basler a2A4504-5gmPRO. 
This camera doesn't work with Matlab GigE Vision neither Genicam hardware support packages.
I hope someone find this useful.

### Requirements:
* [Boost C++ Libraries](http://www.boost.org/) (tested with v1.77)
* [Basler Pylon 6](https://www.baslerweb.com/en/sales-support/downloads/software-downloads/) (tested with v6.2.0.18677 of C++ SDK)
* And of course: a Basler Camera. 
This driver should support any Basler camera, but has only been tested on:
  - a2A4504-5gmPRO - GigE Vision camera

## Build

The MATLAB Basler Camera Driver is built by calling the provided `make.m` file. I'll also make available my results in the reporsitory tags.

## Functions
* `baslerFindCameras` returns a cell array containing the camera index and the camera name.
* `baslerCameraInfo` returns a struct containing all parameters of the selected camera.
* `baslerSetParameter` sets a camera parameter.
* `baslerGetParameter` returns the selected camera parameter.
* `baslerSetROI` sets the region of interest (ROI).
* `baslerPreview` displays a preview image.
* `baslerGetData` captures and returns the selected number of frames.
* `baslerSaveData` captures and saves the selected number of frames to disk.

# Matlab_BaslerCamDriver
A universal MATLAB driver for Basler cameras

Copyright (c) 2015 Hannes Badertscher, ICOM Institute for Communication Systems
at HSR University of Applied Sciences of Eastern Switzerland - [icom.hsr.ch](http://www.icom.hsr.ch)

Until now, interfacing cameras in MATLAB was a cumbersome task. 
MATLAB offers no support for USB3 Vision cameras, and the GigE driver is rather buggy.
This driver package provides an open-source C++ interface between MATLAB and Basler's Pylon interface.

This driver was developed at the ICOM Institute for Communication Systems 
at HSR University of Applied Sciences of Eastern Switzerland, Rapperswil. 

## Disclaimer

Unfortunately, this project is not being actively developed and maintained anymore.
Due to that, it is still required to use Pylon 4 and not the most recent Pylon 5.
If you are interested in updating this driver to Pylon 5 please feel free to contact me.
Further, the camera support in MATLAB has improved significantly since this project was first published - 
I suggest giving the MATLAB Image Acquisition Toolbox a try first.


## License

The MIT License (MIT)

Copyright (c) 2015 Hannes Badertscher and ICOM Institute for Communication Systems
at HSR University of Applied Sciences of Eastern Switzerland - [icom.hsr.ch](http://www.icom.hsr.ch)

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
SOFTWARE.
