## Jenkins Installation And Setup In AWS EC2 Redhat Instnace.
##### Prerequisite
+ AWS Acccount.
+ Create Redhat EC2 t2.medium Instance with 4GB RAM.
+ Create Security Group and open Required ports.
   + 8080 got Jenkins, ..etc
+ Attach Security Group to EC2 Instance.
+ Install java openJDK 1.8+ for SonarQube version 7.8

## Install Jenkins and other packages
sudo hostnamectl set-hostname jenkins
sudo yum install wget -y
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo yum upgrade -y
# Add required dependencies for the jenkins package
sudo yum install java-11-openjdk -y
sudo yum install jenkins -y
sudo systemctl daemon-reload
# start jenkins
# Start Jenkins
# You can enable the Jenkins service to start at boot with the command:
sudo systemctl enable jenkins
#You can start the Jenkins service with the command:=
sudo systemctl start jenkins
# You can check the status of the Jenkins service using the command:
sudo systemctl status jenkins
sudo su - ec2-user
echo "echo of jenkins installation"
