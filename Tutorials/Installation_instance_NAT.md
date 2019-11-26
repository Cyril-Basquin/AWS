Tutorial to configurate an instance NAT on AWS
===================================

# Objectifs:
## Create a VPC (10.10.0.0/16) with:
  - 1 publics subnet: (10.10.1.0/24)
  - 1 private subnet: (10.10.11.0/24)



## Routes Tables configuration::
### Main Route Table (Public subet):
  - Target: local              Destination: 10.10.0.0/16 (VPC)
  - Target: Internet Gateway   Destination: 0.0.0.0/0

### Private Route Table (Private subnet):
  - Target: local             Destination: 10.10.0.0/16 (VPC)
  - Target: nat-instance-id   Destination: 0.0.0.0/0

### NAT Security Group
## Inbound rules
  TYPE  PROTOCOL  Port  IP  
  HTTP  TCP       80    10.10.11.0/24
  SSH   TCP       22    10.10.0.0/16   
  HTTPS TCP       443   10.10.11.0/24   

## Outbond rules
  TYPE  PROTOCOL  Port  IP  
  HTTP  TCP       80    0.0.0.0/0  
  HTTPS TCP       443   0.0.0.0/0  

### Instance creation
Create an AMI NAT  instance on linux OS, activate(something)


### with the transfer tool of PuTTy (pscp), transfer the file key from local to the appropriate <b>file<b> in the remote ec2.
pscp -i c:\Users\breto\Desktop\DSTI\Week_6_AWS\First_putty_key.ppk c:\Users\breto\Desktop\DSTI\Week_6_AWS\AWS_key_pair.pem ec2-user@54.227.120.127:/home/ec2-user/.ssh/id_rsa

### Connection in the public instance (ssh, PuTTy)
Connection to the public instance

### From the public instance, allow readability of the key
chmod 400 ~/.ssh/id_rsa  

### Connection to the private instance using ssh
ssh -i /home/ec2-user/.ssh/id_rsa/AWS_key_pair.pem ec2-user@10.10.11.35
