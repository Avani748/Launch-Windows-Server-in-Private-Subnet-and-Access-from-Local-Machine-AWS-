Launch Windows Server in Private Subnet and Access from Local Machine (AWS)
Overview
This project demonstrates how to securely deploy a Windows Server EC2 instance in a private subnet within an AWS VPC and access it from a local machine using a bastion host. It follows best practices by restricting direct internet access to the private instance.
Architecture
The setup includes:
A custom VPC
One Public Subnet (for Bastion Host)
One Private Subnet (for Windows Server)
Internet Gateway for public access
NAT Gateway (optional) for outbound access
Bastion Host for secure RDP access
Technologies Used
AWS EC2
AWS VPC
Windows Server
Remote Desktop Protocol (RDP)
Implementation Steps
Create a VPC with CIDR block (10.0.0.0/16)
Create Public and Private Subnets
Attach Internet Gateway to VPC
Configure Route Tables
Launch Bastion Host in Public Subnet
Launch Windows Server in Private Subnet (no public IP)
Configure Security Groups for restricted access
Connect to Bastion Host using RDP
Access Private Instance via Bastion Host
Security
Private instance has no public IP
RDP access allowed only through Bastion Host
Security groups restrict unauthorized access
Use Case
This setup is useful for securely managing servers in production environments where direct public access is not allowed.
