# AWS Cloud9 Setup and Web Application Guide

## 1. Set Up an IAM User
- Log in to AWS as the root user.
- Create a new IAM user with AdministratorAccess.
- Download the sign-in details (CSV file) and keep them secure.

## 2. Launch AWS Cloud9 IDE
- Follow the instructions to set up a new environment in Cloud9 with the necessary configurations.
- If you encounter an issue, try switching AWS regions.

## 3. Install Apache Maven and Java
- Run the following commands to install Maven:
  ```bash
  sudo wget https://repos.fedorapeople.org/repos/dchen/apache-maven/epel-apache-maven.repo -O /etc/yum.repos.d/epel-apache-maven.repo
  sudo yum install -y apache-maven
  ```
- Install Amazon Corretto 8 (Java 8):
  ```bash
  sudo amazon-linux-extras enable corretto8
  sudo yum install -y java-1.8.0-amazon-corretto-devel
  ```

## 4. Create the Web Application
- Use Maven to generate a sample Java web app:
  ```bash
  mvn archetype:generate \
     -DgroupId=com.nextwork.app \
     -DartifactId=nextwork-web-project \
     -DarchetypeArtifactId=maven-archetype-webapp \
     -DinteractiveMode=false
  ```

## 5. Modify the Web App
- Edit the `index.jsp` to display your custom message.

## 6. Clean Up Resources
- After completing the project, delete the Cloud9 environment to avoid incurring costs.

