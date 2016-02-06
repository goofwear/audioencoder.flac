# FLAC Audio Encoder add-on for Kodi

This is a [Kodi] (http://kodi.tv) add-on for encoding your music files.

#### CI Testing
* Tarvis-CI for OS X, iOS, Linux [![Build Status](https://travis-ci.org/xbmc/audioencoder.flac.svg?branch=master)](https://github.com/xbmc/audioencoder.flac)
* AppVeyor for Windows [![Build status](https://ci.appveyor.com/api/projects/status/t08n2xs31xhfsxow?svg=true)](https://ci.appveyor.com/project/MartijnKaijser/audioencoder-flac)
* Code analyses for Linux [![Coverity Scan Build Status](https://scan.coverity.com/projects/5120/badge.svg)](https://scan.coverity.com/projects/5120)

## Build instructions

When building the addon you have to use the correct branch depending on which version of Kodi you're building against. 
For example, if you're building the `Jarvis` branch of Kodi you should checkout the `Jarvis` branch of this repository. 
Addon releases are also tagged regularly.

### Linux

1. `git clone https://github.com/xbmc/xbmc.git`
2. `git clone https://github.com/xbmc/audioencoder.flac.git`
3. `cd audioencoder.flac && mkdir build && cd build`
4. `cmake -DADDONS_TO_BUILD=audioencoder.flac -DADDON_SRC_PREFIX=../.. -DCMAKE_BUILD_TYPE=Debug -DCMAKE_INSTALL_PREFIX=../../xbmc/addons -DPACKAGE_ZIP=1 ../../xbmc/project/cmake/addons`
5. `make`

The addon files will be placed in `../../xbmc/addons` so if you build Kodi from source and run it directly 
the addon will be available as a system addon.
