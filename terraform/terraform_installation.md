## INSTALL ON WINDOWS
* Go to https://www.terraform.io/downloads.html
* Download windows 64-bit zip - https://releases.hashicorp.com/terraform/1.4.6/terraform_1.4.6_windows_amd64.zip
* Once downloaded, extract the zip file to downloads directory
* Rename the extracted folder to terraform
* Add to PATH Environment variables 
   1. Open windows explorer, click on PC, click on properties.
   2. Choose  right click on properties, Click on Advanced system settings.
   3. Click on environment variables
   4. Click on Path --> Edit
   5. Add path of directory where you extracted terraform. `C:\Users\<user_name>\Downloads\terraform`
   6. Click on OK, OK, Apply Save.
* Verify Terraform installation
  1. Open Gitbash
  2. Type `terraform version`

## INSTALL ON UBUNTU 
* Create a working directory
   `sudo mkdir -p /opt/terraform`
   `cd /opt/terraform`
* Download Terraform from HasiCorp website
  `sudo wget https://releases.hashicorp.com/terraform/1.4.6/terraform_1.4.6_linux_amd64.zip`
* Install unzip utility
  `sudo apt-get install unzip -y`
* Unzip Terraform Zip file
 `sudo unzip terraform_1.4.6_linux_386.zip`
* Add terraform to PATH
 `sudo mv /opt/terraform/terraform /usr/bin/`
* Verify Terraform version
 `terraform -version`
 
## INSTALL ON RHEL/CENTOS
* `sudo yum install -y yum-utils`
* `sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/RHEL/hashicorp.repo`
* `sudo yum -y install terraform`
* `terraform version`

## INSTALL ON MAC OS
* `brew tap hashicorp/tap`
* `brew install hashicorp/tap/terraform`
* `terraform version`


