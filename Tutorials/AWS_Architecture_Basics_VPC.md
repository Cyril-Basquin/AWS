### Fast Start of an AWS VPC

![VPC_Basics](https://github.com/Cyril-Basquin/AWS/blob/master/Tutorials/Images/Basics_VPC.png)


1. Create a VPC
    + Give it a comprehensive name (VPC_with_NAT_instance_JumpBox_FI)
    + Choose a IPv4 CIDR of at least 16 bytes (10.0.0.0/16)


2. Internet Gateway (IG)
    + Create an IG
    + Attach it to your VPC


3. Create a subnet
    + Name it comprehensively (Public_Subnet)
    + Link it to an existing VPC
    + Choose a Availability Zone (AZ)
    + Choose a IPv4 CIDR (10.0.1.0/24)


4. Route Table (RT)
  + Create a new RT
    + Name it comprehensively (RT_Public_subnet)
    + Attach it to your VPC
  + RT configuration with the IG  
\# In *Route Tables*, select your RT then go to __*Routes*__  ==> __*Edit routes*__ ==> __*Add route*__
    + In destination, write 0.0.0.0/0
    + In target, select *Internet Gateway*, then your IG
