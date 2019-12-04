### Create a jupyter server with ubuntu

##### Create an Ubuntu instance  (ex: ami-04b9e92b5572fa0d1)
In security Group, allow access to port 22 (SSH), and port 8888 (Jupyter notebook)

Connect to your instance
**NOTE:** to connect to an Ubuntu EC-2 instance  
``ssh -i key.pem ubuntu@xxx.xxx.xxx.xxx``  


**Update Ubuntu**  
``sudo apt-get update``    


**Install pip on python3**  
``sudo apt-get install python3-pip``  


**Install Jupyter with pip**  
``sudo pip3 install jupyter``   


**You bin to every ip possible**  
**nohup .... &**: allow you to have access to jupyter even if you close putty  
``nohup jupyter notebook --ip=0.0.0.0 &``


**Copy paste the token url to connect from your browser (see image)**
``cat nohup.out``


![Architecture](https://github.com/Cyril-Basquin/AWS/blob/master/Tutorials/Images/ubuntu_jupyter_get_token.png)  


Paste it in your browser and change the IP with the one of your EC2  
The URL have to be something like that:
http:\\xxx.xxx.xxx.xxx:8888/?token=slkhfbdfkjhvbksdvbkjdfv6d4f54

Start


**NOTE:** with a Linux 2 (CentOS) instance, replace apt-get by yum
