Tutorial to configurate an instance NAT on AWS
===================================

# Objectifs:
## Create a VPC (10.10.0.0/16) with:
  - 2 publics subnet: (10.10.1.0/24 et 10.10.2.0/24)
  - 2 private subnet: (10.10.11.0/24 et 10.10.12.0/24)

## Routes Tables configuration::
### Main Route Table (public):
  - Target: local              Destination: 10.10.0.0/16 (VPC)
  - Target: Internet Gateway   Destination: 0.0.0.0/0

### Private Route Table (Private):
  - Target: local             Destination: 10.10.0.0/16 (VPC)
  - Target: nat-instance-id   Destination: 0.0.0.0/0

### NAT Security Group
# Inbound rules
  TYPE  PROTOCOL  Port  IP
  HTTP  TCP       80    10.10.11.0/24
  SSH   TCP       22    10.10.0.0/16
  HTTPS TCP       443   10.10.11.0/24

# Outbond rules
  TYPE  PROTOCOL  Port  IP
  HTTP  TCP       80    0.0.0.0/0
  HTTPS TCP       443   0.0.0.0/0


https://docs.aws.amazon.com/fr_fr/vpc/latest/userguide/VPC_NAT_Instance.html#EIP_Disable_SrcDestCheck


Create a VPC 10.10


=> Link to see things to do https://www.youtube.com/watch?v=vIGEmrhiuXo
