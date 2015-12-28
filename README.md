# PCSX-Reloaded - A PlayStation Emulator
<p align="center">
<a href="https://pcsxr.codeplex.com/">Homepage</a> | 
<a href="https://pcsxr.codeplex.com/discussions)">Disscusions</a> | 
<a href="https://pcsxr.codeplex.com/workitem/list/advanced">Issue Tracker</a>
</p>

PCSX-Reloaded is a forked version of the dead PCSX emulator, with a nicer
interface and several improvements to stability and functionality.

PCSX-Reloaded uses the PSEMU plugin interface to provide most functionality.
A number of plugins are provided out of the box.

PCSX-Reloaded has an Internal HLE BIOS that can run many games.
However, if you own a real PlayStation, you are able to use your own BIOS image.
PCSX-Reloaded will find it in `~/.pcsx/bios/` or `/usr/share/psemu/bios/` if you
place it there. Using a real BIOS will improve compatibility, especially with
certain games and with theuse of memory cards. The following is an incomplete
compatibility list of games that need a BIOS file to run without issues:
[PCSX-Reloaded incomplete HLE compatibility list](https://pcsxr.codeplex.com/wikipage?title=PCSX-Reloaded%20incomplete%20HLE%20compatibility%20list&referringTitle=Documentation)

## Building
### Windows
Use the solution file `win32/pcsxr.sln` to build PCSX-Reloaded on Windows.

### Linux
Quick compilation & installation guide from Subversion for Ubuntu:

1. `sudo apt-get install subversion autoconf intltoollibtool libsdl1.2-dev libgtk-3-dev libxv-dev libxtst-dev nasm`
2. `svn co https://pcsxr.svn.codeplex.com/svn/pcsxr pcsxr`
3. `cd pcsxr/`
4. `./autogen.sh`
5. `./configure`
6. `make`
7. `sudo make install`
For OpenGL support: install libxxf86vm-dev and add option `--enable-opengl` to `./configure`.

### Mac OS X
To build on Mac OS X, you will need Mac OS X 10.9 or later, with Xcode 6.1
or later. You will also need a version of the SDL2 framework installed in
`/Library/Frameworks/`. Double-click `Pcsxr.xcodeproj` or `Pcsxr.xcworkspace`
in the `macosx` subfolder, select Archive from the Project menu. After the
build is finished, the Organizer window will pop up. Click the export 
button, then select either "signed Application" or just application.

See the `doc/` folder in the source, or `/usr/share/doc/pcsx/` on Debian
systems, for more detailed information on PCSX-Reloaded.
A UNIX manpage is also available.

## Hotkeys

* `F1`: Save state
* `F2`: Switch to next save slot
* `F3`: Load state
* `F4`: Display state screenshot
* `F5`: Toggle SIO IRQ
* `F6`: Toggle Black & White decoders
* `F7`: Toggle XA
* `F8`: Take a game screenshot
* `F9`: Open the Disc tray
* `F10`: Close the Disc tray
* `ESC`: Return to the main window
* `Ctrl 1 to 5`: Save state 1 to 5
* `Alt 1 to 5`: Load state 1 to 5
* `Alt 0`: Load state from last ESC quit
