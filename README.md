Accessing-VM-Using-Cloud NAT

Architecture:
   ![image](https://user-images.githubusercontent.com/85304071/144562541-a689bfa1-88e0-4798-a81b-79f6d6c58750.png)
       



Problem: 
	To make the private instance created without external ip communicate with the internet using cloud NAT.

Purpose:
Accessing VM instance and communicating with internet using cloud NAT without external ip.

Overview:
 The cloud Nat will allow the VM instance which is created in the private subnet to communicate with the internet without external ip and the VM instance which is created in the public subnet can communicate directly with the internet because it has the external ip.

Required resources:
1)	  A VPC network with public and private subnet.
2)	  A firewall
3)	Two instances one with external ip and other without external ip
4)	Cloud NAT to access VM and communicate with internet
5)	Cloud Router
6)	Google compute address

Prerequistes:
          Terraform
         Access to GCP project

Steps:
1)	Create a vpc 
2)	Create two subnets one public and the other one private
3)	Create two instances one in each subnet, one with external ip and other one without external ip
4)	Create a firewall rule to access ssh
5)	Create a google compute address and a cloud router 
6)	Create Cloud NAT which should be created in the same region as that of private subnet region to make the instance which is created in the private subnet to communicate with internet without external ip.



Deployment:
	Clone the repo in terraform directory
	Then initialize terraform build using command
  - > terraform init

  Now after build validate code by running cpmmand
  -	> terraform validate

  Upon successful validation verify deployment plan using command
  -	> terraform plan

  Now to deploy the resources run command
  -	> terraform apply


Output:

 
![image](https://user-images.githubusercontent.com/85304071/144811610-83fbdb4b-7e8f-4ae7-861e-0e7169c40fc2.png)



![image](https://user-images.githubusercontent.com/85304071/144811547-86f721dc-502e-4095-aae2-b3c2469094bf.png)



![image](https://user-images.githubusercontent.com/85304071/144811470-ea910be6-5ca5-4bd2-8502-0e2bffaf97c6.png)



![image](https://user-images.githubusercontent.com/85304071/144811385-89249cb0-fb8b-4d74-97ba-ac804b986309.png)



![image](https://user-images.githubusercontent.com/85304071/144811271-f49db864-49a4-4e02-b595-ad40076a62e4.png)


 

 


 





 
















 

 

 

 






