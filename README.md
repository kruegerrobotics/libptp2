# Fork of libptp2

## Why the fork

This is a fork of the original [libptp2](http://libptp.sourceforge.net/). For developments it was required to move to CMake and to make a few adaptations in the header. However the build and use might be currently not as robust as the original.

Also a **WARNING**: This is work in progress and will either disappear or be communicated back to the authors of the orginial - if this makes sense here.

## How to build

This library is intended for the use on Linux

### Prerequisites

#### libusb

The *libusb* is required to build this library. On Debian systems libusb with lib and headers can be installed with 

``` bash
sudo apt install lib libusb-dev 
```

### Build command

This will clone, build and install this fork of libptp2. If no installation prefix is set via CMAKE_INSTALL_PREFIX then it will install into /usr/local and sudo rigths are required for the install.

``` bash 
git clone https://github.com/kruegerrobotics/libptp2
cd libptp2
mkdir build
cd build
cmake ../
make 
sudo make install
```

Since this fork is development only there will be a lot of warnings.
