### Create and manage Virtual environnement for Jupyter Notebook

**Install pew**
sudo pip3 install pew

**Create a new environnement**
pew new my_new_environnement

**Activate the environnement**
pew workon my_new_environnement

**Install the package ipykernel in your env**
pip3 install ipykernel

**Connect your env to jupyter**
python3 -m ipykernel install --user --name=oasis

**Install package in the virtual environnement**
pip3 install pandas

**Look wich package are installed**
pip3 freeze

**Connect the virtual env to Jupyter**

**Write in a text file the list of your installade packages**
pip3 freeze > CrevetteEnv.txt
