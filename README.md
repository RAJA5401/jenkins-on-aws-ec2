# Jenkins Setup on AWS EC2 (Ubuntu)

🚀 My first DevOps project — I installed and configured Jenkins on an AWS EC2 instance running Ubuntu.

## 🔧 Steps I Followed

1. **Created an EC2 Instance**
   - Type: t2.micro (Free Tier)
   - OS: Ubuntu 22.04
   - Opened ports 22 (SSH) and 8080 (Jenkins) in the Security Group

2. **Installed Jenkins**
   ```bash
   sudo apt update
   sudo apt install openjdk-11-jdk -y
   wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
   sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
   sudo apt update
   sudo apt install jenkins -y
   sudo systemctl enable jenkins
   sudo systemctl start jenkins
