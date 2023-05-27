## INSTALL ON WINDOWS
* Go to https://www.terraform.io/downloads.html
* Download windows 64-bit zip - https://releases.hashicorp.com/terraform/1.0.11/terraform_1.0.11_windows_amd64.zip
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