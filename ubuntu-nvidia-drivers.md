### Symtoms
1. Fresh install of Ubuntu gets stuck after login screen
1. Mouse movement is not smooth on login screen
1. Clt+Alt+F2, shows lot of `PCIe Bus error severity=Corrected` lines

### Solution
1. If you are getting the PCIe Bus error, try this [askubuntu link](https://askubuntu.com/questions/771899/pcie-bus-error-severity-corrected)
1. On login screen, press Clt+Alt+F2 and login using your credentials
1. `sudo add-apt-repository ppa:graphics-drivers`, this will show you a lot of text including the 'Current long lived branch release', in my case it was nvidis-430 (430.30)
1. `sudo apt update`
1. `sudo apt install nvidia-driver-430`
1. Restart PC and try again
