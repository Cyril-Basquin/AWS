Tutorial pour configurer un VPC avec AWS
===================================

# Objectifs:
## Créer un VPC (10.10.0.0/16) avec:
  - 2 serveurs publics: (10.10.1.0/24 et 10.10.2.0/24)
  - 2 serveurs private: (10.10.11.0/24 et 10.10.12.0/24)
   
## Configuration des Route Tables:
### Route Table Principale (public):
  - Target: local              Destination: 10.10.0.0/16 (VPC)
  - Target: Internet Gateway   Destination: 0.0.0.0/0
  
### Route Table secondaire (Private):
  - Target: local             Destination: 10.10.0.0/16 (VPC)
  - Target: nat-instance-id   Destination: 0.0.0.0/0
  
https://docs.aws.amazon.com/fr_fr/vpc/latest/userguide/VPC_NAT_Instance.html#EIP_Disable_SrcDestCheck
  

Create a VPC 10.10
