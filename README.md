# Terraform
here I store all my teraform main.tf files

## for installation

sudo apt-get update && sudo apt-get install -y gnupg software-properties-common

wget -O- https://apt.releases.hashicorp.com/gpg | \
gpg --dearmor | \
sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg


gpg --no-default-keyring \
--keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg \
--fingerprint

echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
sudo tee /etc/apt/sources.list.d/hashicorp.list

sudo apt update

sudo apt-get install terraform

## note 

make sure your master node aws instance should also have awscli in order to connect and send api calls .

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

or

 # sudo apt-get install awscli

## use of terraform

terraform is a infrastructure as a code tool which can be used to do the followings -

- manage any infrastructure
- Track your Infrastructure
- Automate Changes
- Statndardise Configurations
- Collaborate

terraform documentation can be followed from hashicorp website for AWS /azure /other cloud providers to create /tf files


## commands in Terraform

- terraform init  ->   initialize
- terraform plan  ->   dry run
- terraform apply
- terraform destroy

## problem with terraform

- state file is the only source for truth (terraform statefile)
- manual changes cannot be identified and autocorrected i.e. no autohealing
- not a gitops friendly tool

