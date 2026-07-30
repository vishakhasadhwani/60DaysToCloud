# Week2 Linux_ & Networking - Servers & Connectivity (Days 13–19)

## Goal

Launch a virtual machine, SSH into it, serve a web page, and understand basic networking around it.

## Time Commitment

1.5–2 hours per day, 5–7 days.

## What To Expect

By the end of Week 2, you should:
- Be able to launch a VM/instance
- Connect via SSH using a key pair
- Install Nginx and serve a basic HTML page
- Know what VPC/VNet, subnet, and security group/NSG are

You are not expected to design complex network topologies yet.

## Step-by-Step

1.	Launch a VM/instance

	- AWS EC2:
	https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html

	- GCP Compute Engine:
	https://cloud.google.com/compute/docs/instances/create-start-instance

	- Azure Linux VM:
	https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-portal

	- OCI Compute:
	https://docs.oracle.com/en-us/iaas/Content/Compute/Tasks/launchinginstance.htm
	•	Choose a Linux image (Amazon Linux, Ubuntu, Oracle Linux, etc.)
	•	Note where you configure network (VPC/VNet/VCN) and firewall rules.

2.	Understand the network layer

	- AWS VPC:
	https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html

	-	GCP VPC:
	https://cloud.google.com/vpc/docs/vpc

	-	Azure VNets:
	https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview

	-	OCI VCN:
	https://docs.oracle.com/en-us/iaas/Content/Network/Tasks/managingVCNs.htm

		•	Learn what:
		•	VPC/VNet/VCN is
		•	Subnet is
		•	Security Group/NSG is
		•	Draw a small diagram: Internet → VPC/VNet → Subnet → VM.
	

3.	SSH into the VM
	
	-	SSH basics:
	https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys
		•	Generate or download key pair when launching instance
		•	Use ssh -i your-key.pem user@public-ip
		•	Fix permission issues with chmod 400 your-key.pem if needed.

4.	Install Nginx and serve a page

	-	AWS EC2 + Nginx:
	https://docs.nginx.com/nginx/deployment-guides/amazon-web-services/ec2-instances-for-nginx/

	-	GCP Nginx:
	https://cloud.google.com/community/tutorials/nginx-on-compute-engine

	-	Azure Nginx:
	https://learn.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-load-balancer

	-	OCI Nginx:
	https://docs.oracle.com/en/learn/ol-nginx/
		•	Install Nginx
		•	Replace default index.html with your own content
		•	Adjust security group/NSG to allow HTTP/HTTPS
		•	Access via browser using the public IP.

5.	Check logs

	-	AWS EC2 logs:
	https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-console.html

	-	GCP serial port logs:
	https://cloud.google.com/compute/docs/instances/viewing-serial-port-output

	-	Azure boot diagnostics:
	https://learn.microsoft.com/en-us/azure/virtual-machines/boot-diagnostics

	-	OCI serial console:
	https://docs.oracle.com/en-us/iaas/Content/Compute/References/serialconsole.htm

		What you must do!!
		- Check system logs or Nginx logs once
		- See how requests appear.

	Checklist
	- You can launch a VM in your chosen cloud
	- You can SSH into it using a key
	- You can serve a simple web page using Nginx
	- You can describe VPC/VNet, subnet, and security group/NS

## Practice Resources

	AWS:
	https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html
	https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html
	https://docs.nginx.com/nginx/deployment-guides/amazon-web-services/ec2-install-nginx/
	https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys
	https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-console.html

	GCP:
	https://cloud.google.com/compute/docs/instances/create-start-instance
	https://cloud.google.com/vpc/docs/vpc
	https://cloud.google.com/community/tutorials/nginx-on-compute-engine
	https://cloud.google.com/compute/docs/connect/standard-ssh
	https://cloud.google.com/compute/docs/instances/viewing-serial-port-output

	Azure:
	https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-portal
	https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview
	https://learn.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-load-balancer
	https://learn.microsoft.com/en-us/azure/virtual-machines/linux/connect-ssh
	https://learn.microsoft.com/en-us/azure/virtual-machines/boot-diagnostics

	OCI:
	https://docs.oracle.com/en-us/iaas/Content/Compute/Tasks/launchinginstance.htm
	https://docs.oracle.com/en-us/iaas/Content/Network/Tasks/managingVCNs.htm
	https://docs.oracle.com/en/learn/install_nginx_ol8/index.html
	https://docs.oracle.com/en-us/iaas/Content/Compute/Tasks/accessinginstance.htm
	https://docs.oracle.com/en-us/iaas/Content/Compute/References/serialconsole.htm

	What Won’t Work

	Using only the GUI.
	Learn to troubleshoot using the terminal and logs — that’s what makes you independent.
