# DevOps-CICDPipeline
# Connecting a GitHub Repository with AWS: My Second DevOps Project

In this project, I connected a Java web application's source code to a GitHub repository. This project is part of a seven-project series that builds a CI/CD pipeline using AWS services. Here’s how I successfully completed this project!

---

## What I Built

I learned how to use Git and GitHub to manage and track changes to a Java web application hosted on an AWS EC2 instance. I also connected my local repository to GitHub to store the source code in the cloud.

---

## Getting Started

After setting up the EC2 instance and configuring the remote host on VS Code, I was ready to integrate version control into my project. For detailed instructions on setting up an EC2 instance and connecting it to VS Code, refer to my previous blog post [here(https://medium.com/devops-dev/setting-up-a-web-application-on-aws-my-first-aws-devops-project-a95777492c83)].

---

## Step 1: Setting Up Git

1. **Installed Git on the EC2 Instance**:
   ```bash
   sudo dnf update -y
   sudo dnf install git -y
   ```
2. **Verified Installation**:
   ```bash
   git --version
   ```
3. **Set Up Git Identity**:
   ```bash
   git config --global user.name "someshkumar"
   git config --global user.email "somesh1st@gmail.com"
   ```
   - This ensures commits are associated with your name and email.

---

## Step 2: Creating a GitHub Repository

1. **Created a New Repository on GitHub**:
   - Repository Name: `Devops-CICDPipeline`
   - Description: "Java web app set up on an EC2 instance."
   - Visibility: Public
   - Added a README file.

2. **Copied the Repository URL**:
   - Example: `https://github.com/somesh1312/DevOps-CICDPipeline.git`

---

## Step 3: Connecting the Local Repo with GitHub

1. **Initialized a Local Git Repository**:
   ```bash
   git init
   ```
2. **Connected the Local Repository to GitHub**:
   ```bash
   git remote add origin https://github.com/somesh1312/DevOps-CICDPipeline.git
   ```
3. **Staged All Files**:
   ```bash
   git add .
   ```
4. **Committed the Changes**:
   ```bash
   git commit -m "Initial commit with Java web app files."
   ```
5. **Pushed to GitHub**:
   ```bash
   git push -u origin master
   ```
   - If prompted for authentication, I used a GitHub personal access token instead of a password.

---

## Step 4: Making and Pushing Updates

1. **Modified the `index.jsp` File**:
   - Added a new line of HTML code to the file:
     ```html
     <p>If you see this line in GitHub, that means your latest changes are getting pushed to your cloud repo :o</p>
     ```
2. **Staged and Committed the Changes**:
   ```bash
   git add .
   git commit -m "Add new line to index.jsp."
   ```
3. **Pushed the Changes to GitHub**:
   ```bash
   git push
   ```

---

## Step 5: Setting Up GitHub Authentication

1. **Generated a Personal Access Token on GitHub**:
   - Gave it appropriate scopes (e.g., `repo`).
   - Set expiration to 30 days for security.
2. **Used the Token for Authentication**:
   - When prompted for a password, entered the generated token instead.

---

## What I Learned

- **Version Control**: Using Git to track and manage changes in source code.
- **GitHub Integration**: Storing code in a cloud-based repository for collaboration and backup.
- **Authentication Best Practices**: Securing access to repositories using personal access tokens instead of passwords.

---

## Congratulations to Us!

This marks the successful completion of the second project in my DevOps series. The repository is now ready to host and track changes for my Java web application. Stay tuned for the next project where I’ll explore AWS CodeArtifact for managing project dependencies!

---

*Thank you for reading! If you found this post helpful or have any questions, feel free to leave a comment.*

