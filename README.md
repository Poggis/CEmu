# CEmu [![Build Status](https://travis-ci.org/MateoConLechuga/CEmu.svg)](https://travis-ci.org/MateoConLechuga/CEmu)
CEmu is an open-source third-party TI-84 Plus CE / TI-83 Premium CE calculator emulator.  

With a core made in C and GUI in C++ with Qt, it works natively on many platforms. It has even been succesfully tested on web-browsers (JavaScript via Emscripten), the TI-Nspire CX (Ndless SDK), and the Apple Watch.

Here's what it looks like on Mac OS X:  
<a href="https://i.imgur.com/0BJsPoG.png"><img src="https://i.imgur.com/L9nuir2.png" /></div></a>

## License
CEmu is licensed under the [GPLv3](LICENSE).  
_Acknowledgements_: Some CEmu parts are, directly, modified, or inspired, from [z80e](https://github.com/KnightOS/z80e), [Firebird](https://github.com/nspire-emus/firebird), and [QHexEdit2](https://github.com/Simsys/qhexedit2). Their licensing information are available on the [LICENSE](LICENSE) file.

## Downloads
No stable binaries yet as the code keeps changing these days! When available, they'll be here, though: https://github.com/MateoConLechuga/CEmu/releases  
Nightly win32 binaries available here (hosted by pimathbrainiac): http://pimathbrainiac.me/CEmu/

## How to build
After downloading the source (you can clone the repo or just get the zip):

1. Get the [latest Qt5 SDK](https://www.qt.io/download-open-source/#section-3) for your OS.
2. Now you have two options:
  * Open the .pro file with Qt Creator, set it up (default project settings should be fine), and hit Build
  * In a shell, cd to the project folder and type `qmake -r CEmu.pro; make`

You're welcome to [report any bugs](https://github.com/MateoConLechuga/CEmu/issues) you may encounter, and if you want to help, tell us, or send patches / pull requests!


## TODO list
### Core
* Implement unknown port range (0xDXXX)
* Implement USB (0xDXXX appears to be a part of this as well)
* Add more flash handlers
* other bug fixes
* ...

### Overall features
* More robust and complete variable transfer (Calc <-> Computer)
* Emulation speed setting
* ...

### GUI
* Window for configuring keybindings
* HD Icon
* Fix single GIF frame output
* Plan for 83PCE / 84+CE differences (2 keypad setups, "skins", etc.)
* More translations (for now, it's available in English and French).
* ...

## In the future...
* Make a web-based version of CEmu, like there’s a web-based version of z80e for trying out KnightOS. _Compiling the CEmu core to JavaScript (and later WebAssembly), using Emscripten, is already known to work_
* Think about CEmu's core’s integration on third-party projects, like TI-Planet's Project Builder - for instance, in C projects, in order to directly test the program, and eventually have live source-level debugging!
* Look at [this gdb-z80](https://github.com/legumbre/gdb-z80) project (code from 2011...) ; try to see if it can be updated for eZ80, and used with a CEmu GDB stub. Mainlining such code is highly preferable.
* ...
