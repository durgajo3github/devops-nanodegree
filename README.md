# devops-nanodegree
cloud devops nanodegree 

The following document contains instructions on how to deploy a highly available web application using AWS CloudFormation.

Infrastructure Deployment
The application infrastructure consists of deploying the following stacks:

Network. This includes VPC, two pairs of public and private subnets, Internet Gateway, NAT Gateways and Routing Tables for public and private subnets with associations.
Bastion hosts (Optional). These are EC2 instances for troubleshooting of application web servers.
Application services. In particular, Load Balancer, web servers and corresponding autoscaling, target and security groups.
Create infrastructure

To create the infrastructure stack run the following commands in the same order as below:

./create.sh udagram-infrastack infrasetup.yml infraconfig.json

./create.sh udagram-appstack applaunchconfig.yml ename.json

Verify deployment
To check whether the web application is running, follow the web application public URL, which could be found in output exports of pplaunchconfig cloud formation stack.

Output(working URL to verify the webapp):
http://udagr-webap-axhozo1hqolm-483606527.us-west-2.elb.amazonaws.com/
