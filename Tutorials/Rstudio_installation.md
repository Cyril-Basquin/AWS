### Script to install RStudio  on a EC2 instance

At the creation of your EC2 instance (ex: the 'first one' Linux 2 ami-00068cd7555f543d5)  
Copy paste this script at Step3

\#!/bin/bash  

**\# Linux update**  
``sudo yum update -y``  

**\# R installation**  
``sudo amazon-linux-extras install R3.4 -y``  

**\# Rstudio installation (For Unix with Cent OS as OS).**  
``wget https://download2.rstudio.org/server/centos6/x86_64/rstudio-server-rhel-1.2.5019-x86_64.rpm  
sudo yum install rstudio-server-rhel-1.2.5019-x86_64.rpm -y``  

**\# Create a Rstudio instance with 'username' as username ans 'password' as password.**    
``sudo useradd username  
echo username:password |sudo chpasswd``
