### On Ubuntu
1. sudo apt install x11vnc
1. x11vnc -storepasswd
1. x11vnc -usepw, note the port in the output : 
    ```
    The VNC desktop is:      Workbench:0
    PORT=5900
    ```
1. Install RealVNC Viewer on MacOS and setup a new connection using the ip, port and password from above

```RealVNC, TightVNC, etc. Are usually used like RDP on Windows, where you get your own separate X session when you connect. X11VNC is more commonly used when you want to share an existing X session (e.g. So you can see/control what's going on on the desktop, including users logging in and out).``` - [source](https://lasopastudios207.weebly.com/x11vnc-vs-tigervnc.html#:~:text=x11vnc%20does%20not%20create%20an,alternatives%20such%20as%20TightVNC%20Server)

https://ubuntuforums.org/showthread.php?p=9841085

sudo apt install tigervncserver

tigervncpsswd

tigervncserver
