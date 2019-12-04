### Create a jupyter server with ubuntu

##### Ubuntu AMI used: ami-04b9e92b5572fa0d1

**NOTE:** to connect to your Ubuntu EC-2 instance  
ssh -i key.pem ubuntu@xxx.xxx.xxx.xxx


##### Connect to your instance
**Update Ubuntu**  
sudo apt-get update  

**Check the presence of python3**  
python  

**Install pip on python3**  
sudo apt-get install python3-pip  

**Install Jupyter**  
sudo pip3 install jupyter  

**You bin to every ip possible**  
jupyter notebook --ip=0.0.0.0  

**Copy paste the given URL**  
http://ip-10-10-10-10:8888/?token=.....  

Paste it in your browser  

Change the IP with the one of your EC2  

Start  


**To summarize: 4 commands line to launch a Jupyter Notebook**    
sudo apt-get update -y
sudo apt-get install python3-pip -y
sudo pip3 install jupyter

jupyter notebook --ip=0.0.0.0
