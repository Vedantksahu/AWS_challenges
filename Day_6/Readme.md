# Node.js Website Deployment Using Docker on AWS EC2

# Overview

This repository contains a Node.js web application that runs inside a Docker container and is deployed on an AWS EC2 instance.
The goal is to provide a simple guide for setting up a containerized web application on AWS.

---------------------------------------------------------------------------------------------------------------------

# Getting Started

Follow these steps to clone the repository, build the Docker image, and run the application.

# Prerequisites

Ensure you have the following installed:

# Git

# Docker

# Node.js

# AWS EC2 instance (Ubuntu or Amazon Linux 2)


---------------------------------------------------------------------------------------------------------------
# Step:-1

1. Clone the Repository

$git clone 
$cd 

# Step:-2

$npm install

# Step:-3
Build and Run the Docker Container Locally/

# Build the Docker image
docker build -t nodejs-docker-app .

# Run the container
docker run -p 3000:3000 nodejs-docker-app

# Step-4 

Access the app at: http://localhost:3000

# Step-5:-

Deploying on AWS EC2

ssh -i your-key.pem ubuntu@your-ec2-public-ip

# Step-6:-

sudo apt update && sudo apt install -y docker.io  # Ubuntu  
sudo systemctl start docker  
sudo systemctl enable docker  
sudo usermod -aG docker $USER  

# Step-7:-

$sudo apt-get reboot


# Relogin in the system, as after changing the usergroup the system needs reboot.

# Step-8:- 

docker build -t nodejs-docker-app .
docker run -d -p 80:3000 nodejs-docker-app

# Step-9:-

Varify the deployment-

Open http://your-ec2-public-ip in a browser.

Output must be:-

# ✅ "Hello, World! This is a Node.js app running in Docker on EC2!"

-----------------------------------------------------------------------------------------------------------------------------------


























