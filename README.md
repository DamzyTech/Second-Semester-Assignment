# Cloud Engineering Second Semester Project – AltSchool Tinyuka 2024

This README documents the steps I followed to complete the Cloud Engineering second semester project, including server provisioning, web server setup, and deployment of a dynamic landing page.

---

## Project Overview

As part of the second semester assessment, I was tasked with provisioning a Linux server, configuring a web server, and deploying a dynamic, styled landing page to showcase a startup idea.

---

## 1. Server Setup (AWS EC2)

- I used **Amazon Web Services (AWS)** to provision a new EC2 instance titled **"MY Web Server"**.
- Configured **inbound traffic rules** to allow:
  - Port 22 (SSH)
  - Port 80 (HTTP)
  - Port 443 (HTTPS)
- Generated an SSH key pair and connected to the instance via **VS Code terminal**.
- Once connected, I created a working directory:
  ```bash
  mkdir second_semester_exam
  cd second_semester_exam

## 2. Web Server Setup (Nginx)
- I chose Nginx as the web server and installed it with the following steps:

1. sudo apt update
2. sudo apt install nginx -y
3. sudo systemctl start nginx
4. sudo systemctl enable nginx
5. sudo systemctl status nginx

- Opened a browser and visited my server’s public IP:
http://18.130.178.12/
- The default Nginx welcome page confirmed a successful installation.

## 3. Deployment
### Landing Page Development
- Developed a landing page for an AI healthtech startup called "Wellness".
- The landing page includes:
1. A navbar and footer
2. Social media icons
3. A short pitch for the startup
4. A professional bio highlighting my skills and background
5. Styled using CSS and Tailwind CSS for a clean, modern look.
### GitHub Integration
- Initialized a Git repository locally and pushed the project to GitHub using the following commands:
1. git init
2. git add .
3. git commit -m "Initial commit"
4. git remote add origin 
5. git push -u origin master
### Deploying to the Server
- SSH’ed back into the AWS Linux server.
- Cloned the GitHub repository:
git clone 
- Copied the index.html file to Nginx’s default web directory: "sudo cp index.html /var/www/html/"
- Then I visited http://18.130.178.12/ again and confirmed that my landing page was successfully deployed
### 🌍 Live Page
- 🔗 URL: http://18.130.178.12
### Screenshot of Deployed Page
<img width="953" alt="image" src="https://github.com/user-attachments/assets/4bff055e-2324-4021-ad9e-66afb1047337" />
