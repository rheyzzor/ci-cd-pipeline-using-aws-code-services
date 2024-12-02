# Build a Web App using AWS Cloud9

## Overview
This project demonstrates how to use AWS Cloud9, a cloud-based IDE, to create a simple Java web application. The app was customized by editing the `index.jsp` file to display dynamic content.

## Steps
1. **Set up an IAM User**  
   Created an IAM user with `AdministratorAccess` for full access to AWS resources.

2. **Launch AWS Cloud9 IDE**  
   - Used Cloud9 to write, debug, and deploy the app without local setup.

3. **Install Maven and Java**  
   - Installed Maven to manage project dependencies and Java (Amazon Corretto 8) for application development.

4. **Create the Web App**  
   Ran the following command:
   ```bash
   mvn archetype:generate \
   -DgroupId=com.nextwork.app \
   -DartifactId=nextwork-web-project \
   -DarchetypeArtifactId=maven-archetype-webapp \
   -DinteractiveMode=false
