1. Install anaconda using the shell scripts ( wget .. )
2. reboot
3. `jupyter notebook --generate-config`
4. update `vim /home/kaustubh/.jupyter/jupyter_notebook_config.py`
  4.1 c.NotebookApp.open_browser = False  
  4.2 c.NotebookApp.port = 80  
  4.3 c.NotebookApp.ip = '<static-ip>'  
5. `jupyter server password`
6. Create a jupyter service in systemd : https://janakiev.com/blog/jupyter-systemd/
  
  
