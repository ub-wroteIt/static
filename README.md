# static
This repository for the demo purpose. Jenkins job and functionality will be explored with help of the this repo

## Requirements
Need to have AWS account & Github account.

## Installation 
setup jenkins on Ubuntu based EC2 instance. follow the following steps in order to install it on ubnuntu machine.
```
# Step 1 - Update existing packages
sudo apt-get update

# Step 2 - Install Java
sudo apt install -y default-jdk

# Step 3 - Download Jenkins package. 
# You can go to http://pkg.jenkins.io/debian/ to see the available commands
# First, add a key to your system
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -

# # Step 4 - Add the following entry in your /etc/apt/sources.list:
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'

# # Step 5 -Update your local package index
sudo apt-get update

# Step 6 - Install Jenkins
sudo apt-get install -y jenkins

# Step 7 - Start the Jenkins server
sudo systemctl start jenkins

# Step 8 - Enable the service to load during boot
sudo systemctl enable jenkins
sudo systemctl status jenkins
```

### Further Steps 

1. Install Blue Ocean & pipeline-aws" Plugin into jenkins.
2. Set up AWS credentials in Jenkins
3. Set up a GitHub Repository
4. Set up S3 Bucket
5. Trigger the scan the Repository Now option from left side bar of jenkins.
