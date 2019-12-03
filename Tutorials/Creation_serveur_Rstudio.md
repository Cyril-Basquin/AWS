# Script to create an EC2 instance and configurate it to launch an sever with R on it


#!/bin/bash  

## Mise à jour de l'installation de l'instance  
sudo yum update -y  

## Installation de R    
sudo amazon-linux-extras install R3.4 -y  

## Installation de Rstudio (For Unix with Cent OS as OS).  
wget https://download2.rstudio.org/server/centos6/x86_64/rstudio-server-rhel-1.2.5019-x86_64.rpm  
sudo yum install rstudio-server-rhel-1.2.5019-x86_64.rpm -y  

## Création d’une instance RStudio server avec « username » comme nom d’utilisateur et « password » comme mot de passe.   
sudo useradd username  
echo username:password |sudo chpasswd
