### On Ubuntu
1. sudo apt install x11vnc
1. x11vnc -storepasswd
1. x11vnc -usepw, note the port in the output : 
    ```
    The VNC desktop is:      Workbench:0
    PORT=5900
    ```
1. Install RealVNC Viewer on MacOS and setup a new connection using the ip, port and password from above
