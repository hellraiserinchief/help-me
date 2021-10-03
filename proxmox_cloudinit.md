
Image used : https://cloud-images.ubuntu.com/releases/focal/release/ubuntu-20.04-server-cloudimg-amd64-disk-kvm.img 

After following the instructions given on the proxmox [cloud init support page](https://pve.proxmox.com/wiki/Cloud-Init_Support), I was able to spawn the vid 123 VM.
I did not follow the network instructions. Unsurprisingly, the network was not connected. To bring 'UP' the network on boot, I had to add `firewall=1` in network device settings in hardware tab.
I also needed to add `ip=dhcp` to cloud-init ipconfig. This was enough to get the VM and IP.

But I was still unable to ssh into the VM, getting the following errors: ( in both host and vm's /var/logs/auth.log )
```
Unable to ssh xxx.xxx.xxx.xxx : Permission denied (publickey) / Connection closed by ::xxx [preauth]
```

Looks like the image have `PasswordAuthentication` no in `/etc/ssh/sshd_config`. changing that to yes and `sudo service ssh reload` solved the problem.

How to save cloud init configs in a snippet : https://gist.github.com/aw/ce460c2100163c38734a83e09ac0439a
