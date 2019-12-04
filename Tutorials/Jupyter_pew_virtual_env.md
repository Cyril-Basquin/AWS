### Create and manage Virtual environnement for Jupyter Notebook

**Install pew**
``sudo pip3 install pew``

**Create a new environnement**  
Note: Do not create an env when you are in an env or they will be nested  
``pew new my_new_environnement``

**Activate the environnement**  
Note: by defaut you enter an env after its creation  
``pew workon my_new_environnement``

**Install the package ipykernel in your env**  
Note: ipykernel allow you to access your env in jupyter
``pip3 install ipykernel``

**Connect your env to jupyter**  
python3 -m ipykernel install --user --name=oasis

**Refresh your browser, then you can connect to your env**  


#### Save and load the packages of an environnement
**To see which packages are installed**  
``pip3 freeze``  


**Write in a text file the list of your installed packages**  
``pip3 freeze > CrevetteEnv.txt``  


**Install all packages save in a text file**  
``pip3 install -r CrevetteEnv.txt``
  
