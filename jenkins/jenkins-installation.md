## Jenkins Installation And Setup In AWS EC2 Redhat Instnace.
##### Prerequisite
+ AWS Acccount.
+ Create Redhat EC2 t2.medium Instance with 4GB RAM.
+ Create Security Group and open Required ports.
   + 8080 got Jenkins, ..etc
+ Attach Security Group to EC2 Instance.
+ Install java openJDK 1.8+ for SonarQube version 7.8

### Change hostname 
sudo hostnamectl set-hostname jenkins
sudo su - ec2-user

### Install wget, git and java
sudo yum install wget -y
sudo yum install java-11-openjdk

### Install Jenkins (Configure yum by adding Jenkins repo and import repo GPG keys)
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io-2023.key
sudo yum upgrade

## Install Jenkins
sudo yum install jenkins -y

### Start, Enable, Check Status of Jenkins
sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins

### Get Initial Password of Jenkins
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
