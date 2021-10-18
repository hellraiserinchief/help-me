1. Install anaconda using the shell scripts ( wget .. )
2. reboot
3. `jupyter notebook --generate-config`
4. update `vim /home/kaustubh/.jupyter/jupyter_notebook_config.py`
  4.1 c.NotebookApp.open_browser = False  
  4.2 c.NotebookApp.port = 80  
  4.3 c.NotebookApp.ip = '<static-ip>'  
5. `jupyter server password`
6. Create a jupyter service in systemd : https://janakiev.com/blog/jupyter-systemd/
  
  ```
[Unit]
After=network.service
Description=Jupyter Notebook

[Service]
Type=simple
ExecStart=/home/<user>/anaconda3/bin/python3 -m jupyter notebook
User=<user>
Group=<user>
Restart=always
RestartSec=10

[Install]
WantedBy=multi-user.target
```

  This worked ok, till I needed to use conda environments as jupyter kernels. I followed conda-env-as-jupyter-kernel.md, but the envs were not whowing up in jupyter. `journalctl` command showed the following error : 
  
  ```
Oct 18 17:27:14 ubuntu start_jupyter.sh[19509]: [E 17:27:14.419 NotebookApp] [nb_conda_kernels] couldn't call conda:
Oct 18 17:27:14 ubuntu start_jupyter.sh[19509]:     [Errno 2] No such file or directory: 'conda'
Oct 18 17:27:14 ubuntu start_jupyter.sh[19509]: [I 17:27:14.421 NotebookApp] [nb_conda_kernels] enabled, 0 kernels found
  ```
  I created the follwoing script and called it from the service instead  ( after `chmod +x ..` ):
  
  ```
#!/bin/bash

source /home/kaustubh/.bashrc
export PATH=/home/kaustubh/anaconda3/bin/:$PATH
/home/kaustubh/anaconda3/bin/python3 -m jupyter notebook
  ```
  
  If anyone has a better soln, I am all ears.
  
