Setting up a macOS -> Linux VNC is useful for programming.
You can run your editor directly on the Linux machine that will end up running your code.
The build toolchains on Linux are more robust than on macOS.

The annoying thing typically is getting the keyboard mapping just right.

This is what works for me going from macOS 10.15 -> Ubuntu 18.04:

1. Use TigerVNC as both the viewer (on macOS) and the server (on Linux). https://www.tigervnc.org
2. Get a version of TigerVNC that supports the `-RawKeyboard` parameter. You can check with `vncserver --version` to see whether the one you have supports it. This is essential.
3. Start `gnome-session &` in `~/.vnc/xstartup`
4. Don't modify the keyboard with `xmodmap`.
5. Install `gnome-tweak-tool`.
6. Enable Gnome Tweak Tool > Keyboard & Mouse > Additional Layout Options > Alt/Win Key behavior > "Meta is mapped to left win".
