Building a three -Tier Infrastructure with Terraform in AWS 

Overview 
One of the many beauties of the cloud is the ability to deploy applications across multiple data centers. This action makes the applications highly available and as a result enables them to have a high tolerance for failures 

In this project, we would be deploying a secure highly available website using a 3-tier infrastructure with a cluster of private and public subnets using terraform as code. 
Our webservers and Elastic load balancers will span across 2 availability zones in order for us to achieve high availability. 

To get started let’s begin by going over certain concepts that would help solidify our understanding of the “essence” of this project as well as some key concepts and explanations.  

Objectives
At the end of this project we would have successfully done the following 

-	Apply infrastructure changes in Terraform 
-	Configure all the network and security infrastructure needed to deploy a highly available website
-	Destroy infrastructure managed by Terraform

To successfully do this  here is an overview of how we would accomplish the project 

1.	Deploy a VPC with CIDR 10.0.0.0/16.
2.	Create 2 public subnets with CIDR 10.0.1.0/24 and 10.0.2.0/24, We would also create a  private subnet with CIDR ‘10.0.3.0/24’.
3.	Create an RDS MySQL instance.
4.	Create a Load Balancer that direct traffic to the public subnets.


The 3 -tiered Architecture 

The 3-tiered architecture is simply a software application that carefully organizes 3 layers of logical and physical computing. These layers are named ;the presentation tier (user interface), the application tier(data processing ) and the data tier (data storage and management). 
Each tier runs its own infrastructure and can be developed simultaneously. 



Why use terraform rather than AWS management Console?

I am sure you are wondering? “Why can’t I just go to the AWS management console and spin this up?”. To answer this, I start off by saying, Yes, it is possible to do this. But it is not best practice. 

However it is worthy to note that we can also use AWS CloudFormation, a native AWS tool to provision resources in simple code which even administrators can grasp. 


Prerequisite
In order to successfully complete these project, you would need the following 
-	Terraform successfully installed 
-	AWS free tier account 
-	Visual Studio Code 

Benefits of three-tier architecture
•	Faster development
•	Improved scalability
•	Improved reliability
•	Improved security

Step – by Step Guide on project 

In order to achieve this, you must ensure that you you properly script to create each of the following:

1.	VPC and Subnets 
2.	Internet Gateway and Route table 
3.	Webservers 
4.	Security Groups  and 
5.	RDS Instance 

