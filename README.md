Beautiful Tourist Place Website - DevOps Mini Project
Project Overview

Beautiful Tourist Place is a responsive tourism website developed using HTML and CSS. The website showcases attractive tourist destinations through an informative layout and image gallery. The project demonstrates the implementation of DevOps practices including Git, GitHub, Docker, Jenkins, and Ansible for automated deployment.

Features
Responsive website design
Attractive user interface
Tourist place information section
Image gallery showcasing destinations
Docker containerized deployment
Jenkins CI/CD pipeline integration
Automated deployment using Ansible
Technologies Used
Frontend
HTML5
CSS3
DevOps Tools
Git
GitHub
Docker
Jenkins
Ansible
Ubuntu (WSL)
Project Structure
DevOpsMiniProject75/
│
├── index.html
├── style.css
├── Dockerfile
├── Jenkinsfile
├── deploy.yml
├── images/
└── README.md
Docker Setup
Build Docker Image
docker build -t portfolio-app .
Run Docker Container
docker run -d -p 8080:80 portfolio-app
Access Website
http://localhost:8080
Jenkins Pipeline

The Jenkins pipeline performs the following tasks:

Build Docker Image
Stop Existing Container
Remove Existing Container
Deploy New Container
Verify Deployment
Ansible Deployment

Execute the deployment playbook:

ansible-playbook deploy.yml

The playbook automatically:

Stops old containers
Removes old containers
Deploys a new container
Verifies deployment
