#### create the workspace
```
$ export ML_PATH="$HOME/ml"      # You can change the path if you prefer
$ mkdir -p $ML_PATH
```

If you would like to work in an isolated environment (which is strongly recommended so that you can work on different projects without having conflicting library versions), install virtualenv8 by running the following pip command (again, if you want virtualenv to be installed for all users on your machine, remove --user and run this command with administrator rights):
```
$ python3 -m pip install --user -U virtualenv
```

Now you can create an isolated Python environment by typing this:
```
$ cd $ML_PATH
$ virtualenv my_env
```

Now every time you want to activate this environment, just open a terminal and type the following:
```
$ cd $ML_PATH
$ source my_env/bin/activate # on Linux or macOS
$ .\my_env\Scripts\activate  # on Windows
```

To deactivate this environment, type `deactivate`. While the environment is active, any package you install using pip will be installed in this isolated environment, and Python will only have access to these packages (if you also want access to the system’s packages, you should create the environment using virtualenv’s --system-site-packages option). Check out virtualenv’s documentation for more information.


#### install all the required modules and their dependencies
```
$ python3 -m pip install -U jupyter matplotlib numpy pandas scipy scikit-learn
```

#### check your installation
```
python3 -c "import jupyter, matplotlib, numpy, pandas, scipy, sklearn"
```
