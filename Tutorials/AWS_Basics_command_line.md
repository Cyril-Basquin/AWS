### Access to your instance with SSH

Once you created an EC2 instance, to access it through the command prompt  
(xxx.xxx.xxx.xxx is the IP provided by AWS)  

For a Linux 2 AMI (=CentOs)   
``$ ssh -i key.pem ec2-user@xxx.xxx.xxx.xxx``

For an ubuntu AMI:  
``$ ssh -i key.pem ubuntu@xxx.xxx.xxx.xxx``

Note: key.pem is the Access key of your instance.  
Note: This command implies that your are located in the folder where you key is:  
``$ cd c:\Wher\ever\you\put\the\key``

Otherwise you can use:  
``$ ssh -i c:\The\full\path\to\your\key.pem ec2-user@xxx.xxx.xxx.xxx``

Alternative: use PuTTy


### Transfer files to your instance

``$ scp -i key.pem file_that_you_want_to_transfer.txt ec2-user@xxx.xxx.xxx.xxx:rename_your_file_if_you_want.txt``

Alternative: use WinSCP


### Folder and file access
``
ls
pwd
cd folder
cat file
``
