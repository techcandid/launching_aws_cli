# Launching an AWS EC2 Instance using the CLI

This guide explains how to launch an Amazon Web Services (AWS) EC2 instance using the command line interface(CLI)

## Prerequisites

- AWS CLI installed and configured
- AWS account with approriate permission 

### Initial setup
- firstly, get your --image-id : This can be gotten from the AMI catalogue of the EC2 dashboard 
(ami-*******************).
![Alt text](<Screenshot (118)-1.png>)

- secondly,creating/getting a key pair:  This can be gotten from the 'Network and security' section of the EC2 dashboard then click on create key pairs and follow through with the instructions.
![Alt text](<Screenshot (119)-1.png>)

- Thirdly, creating/getting a key pair:This can be gotten from the 'Network and security' section of the EC2 dashboard then click on security groups, click on create new security group and follow through with the instructions.
![Alt text](<Screenshot (120).png>)

- lastly, creating/getting a subnet:This can be gotten from the 'subnet' section of the VPC dashboard then click on create subnet and follow through with the instructions.
![Alt text](<Screenshot (121).png>)

#### Launching the EC2 instance
-  To launch an EC2 instance , use the 'aws ec2 run-instances' command in your AWS CLI terminal:
aws ec2 run-instance --image-id ami-xxxxxxxxxxx --count 1 --instance-type t2.micro --key-name Mykeypair --security-group-ids sg-xxxxxxxxx --subnet-xxxxxx
![Alt text](<Screenshot (122).png>)

**congratulations you have successfully launched an instance**