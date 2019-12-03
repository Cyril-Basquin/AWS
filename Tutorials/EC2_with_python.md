Script to launch an EC2-instance with python3

Launch a public instance with:
  - IAM admin role
  - IP
  - The script below (to update linux and install python3)


#!/bin/bash
sudo yum update -y
sudo yum install python3 -y

---------------------------------------
# Connect to you EC-2 instance then launch those 4 command lines:

  1) Install virtualenv (tools that allow to create virtual environnement for python)
  2) Create a directory venv and enter in it
  3) Create the virtual env in venv

pip3 install --user virtualenv
mkdir venv
cd venv
virtualenv -p /usr/bin/python3 python3

# Activate the previously created env
source /home/ec2-user/venv/python3/bin/activate

# Install boto3 in our python environnement
pip install boto3

# Start python
python
