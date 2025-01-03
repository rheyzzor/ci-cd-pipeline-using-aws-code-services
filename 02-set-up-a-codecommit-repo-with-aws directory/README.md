# Set up a CodeCommit Repo with AWS Guide

## 1. Create AWS Cloud9 Setup and Web Application
- Check [01-build-web-app-using-aws-cloud9](./01-build-web-app-using-aws-cloud9/)

## 2. Create a CodeCommit Repository
- Go to the CodeCommit console and create a new repository:
  - **Name**: nextwork-web-project
  - **Description**: A web application for the NextWork home page.
  - **Tag**: team=devops

## 3. Set Up Git and Push Code
- **In Cloud9, configure Git with your name and email:**

    ```bash
    git config --global user.name "your name"
    git config --global user.email "your email"
    ```

- **Initialize a Git repository:**

    ```bash
    git init -b main
    ```

- **Add the CodeCommit repository as the remote origin:**

    ```bash
    git remote add origin <HTTPS CodeCommit repo URL>
    ```

- **Push the changes to CodeCommit:**

    ```bash
    git add .
    git commit -m "Initial commit. Updated index.jsp."
    git push -u origin main
    ```
