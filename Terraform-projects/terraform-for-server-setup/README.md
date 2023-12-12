# IACBluePrints


Before creating the Jenkins using Terraform. There are steps that needs to be done.

1) go to the EC2 dashboard and scroll down to the Key Pairs link inside Network & Security menu.
Click the “Create key pair” button. Give a name like “jenkins-server-key”. With the rest of the form fields as default, download the pem file and set its permission to 400.
chmod 400 jenkins-server-key.pem is the command to set the permission.

2) We are going to use the latest image of Amazon Linux 2 for our Jenkins server instance. If you go to the EC2 dashboard and select Amazon Linux 2, you see the following details:

Go to your Ec2 dashboard and when you click on launch instance it will ask for which OS we need to create the server. So, mentioned above Linux is required. Copy the Amazon linux name and replace in filters values column in Server.tf.

3) Now all the terraform files are ready to run. Before running the terraform files , Please install terraform in your local machine.
4) to initialize the Terraform environment - please execute the command "terraform init"
5) to see how many resources will be created - please execute the command "terraform plan"
6) to create all the resources in aws - please execute the command "terraform apply"

please make sure that you execute the above command under the directory where all your terraform files are there.

After finishing this, we will be able to see jenkins server created in an EC2 instance in AWS with terraform, AWS CLI, java. It also creates a VPC with subnets
