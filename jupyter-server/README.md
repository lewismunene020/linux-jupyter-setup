
# Installation
```
#!/bin/bash

virtualenv .venv 

source .venv/bin/activate

sudo  apt  install  jupyter-core

pip install  jupyter 


# setting up jupyter notebook config file
jupyter notebook --generate-config
cd ~/.jupyter || exit

```

# Setting  up password  to login to jupyter  notebook 
```
jupyter notebook password

# output

Enter password: 
Verify password: 
[NotebookPasswordApp] Wrote hashed password to /home/<folder>/.jupyter/jupyter_notebook_config.json

```

# running a jupyter server 
```
  jupyter notebook  --port='enter your  port here'
  
```


# Allow remote connections

```
# allowing  jupyter remote access
nano jupyter_notebook_config.py
```

## Old
```

# c.NotebookApp.allow_remote_access = False
# c.NotebookApp.ip = 'localhost'
```
## New 
```
c.NotebookApp.allow_remote_access = False
c.NotebookApp.ip = '*'
```

# Allowing root access to   the jupyter  notebook
```
# c.NotebookApp.allow_root = False

<!-- new configuration -->
c.NotebookApp.allow_root = True
```


# Setting Jupyter to  load on boot

```
 echo "jupyter notebook --config=/home/lewis/.jupyter/jupyter_notebook_config.py --port=10000" >> ~/.bashrc 
```
### Use  your desired port  to replace ```--port=10000 ```



# acknowledgments 
- [Jupyter Setup ](https://iconof.com/how-to-setup-a-jupyter-notebook-ubuntu-server/)



