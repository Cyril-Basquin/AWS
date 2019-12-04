### Create a jupyter server with ubuntu

##### Ubuntu AMI used: ami-04b9e92b5572fa0d1

**NOTE:** to connect to your Ubuntu EC-2 instance  
ssh -i key.pem ubuntu@xxx.xxx.xxx.xxx


##### Connect to your instance
**Update Ubuntu**  
sudo apt-get update  

**Install pip on python3**  
sudo apt-get install python3-pip  

**Install Jupyter with pip**  
sudo pip3 install jupyter  

**You bin to every ip possible**  
**nohup .... &**: allow you to have access to jupyter even if you close putty  
nohup jupyter notebook --ip=0.0.0.0 &

**Copy paste the token url to connect from your browser**
cat nohup.out

![Architecture](https://github.com/Cyril-Basquin/AWS/blob/master/Tutorials/Images/ubuntu_jupyter_get_token.png)  


Paste it in your browser and change the IP with the one of your EC2  

Start


**NOTE:** with a Linux 2 (CentOS) instance, replace apt-get by yum
