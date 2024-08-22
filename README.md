# vpc-project
In this project we create a VPC, then we deploy the servers in two availability zones by using Auto scaling group and Application Load balancer. We deploy servers in private subnets. The servers receive requests through the Load Balencer.The servers connect to internet using a NAT gateway. To improve resiliency, you deploy the NAT gateway in both Availability Zones.
*In this project we are running a simple python application in one of the ec2 instances
steps involveds :
1.we create a vpc in which we create 2 Availability zones,and in each of the az we deploy a public and a private subnets .the subnets are attached to the route tables .
2.The public subnets are attached to the internet gateways in eaach az 
3.we deploy a NAT gate ways in each AZ
4 For the safety we lauch the ec2 instances inside the private subnets and we deploy the python application inside the ec2
5. create a autoscaling group using which the ec2 instances are created min value is 1 and max is 4
6. to log into the ec2 we have to create a bastion host or jump server in the public subnet.bastion host is the neww ec2 instance launched in public subnet
  *after creation of bastion copy the pem file in laptop to the bastion using the command scp -i 
  *log into the bation host 
  *after that ssh into the ec2 instance using the private ip adress
  *once you ssh into the instance1 create a html file hat displays "THIS IS MY EC2 IN PRIVATE SUBNET"
  *Then install python3 -m http.server 8000
  install the python app in port 800
7 create application load balancer and inside it create atargert group 
the using the load balancer address at port 8000 try to access from outsidde and the html page will be displayes
this demonstartes hoe we deploy servers  which are inside the vpc created.
  
