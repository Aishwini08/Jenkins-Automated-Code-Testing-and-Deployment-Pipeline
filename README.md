🚀 Jenkins CI/CD Pipeline with Docker & Node.js

This project demonstrates an end-to-end CI/CD pipeline using Jenkins to automate build, test, and deployment of a Node.js application on AWS EC2 using Docker and PM2.

🛠️ Tech Stack
Node.js
Jenkins
Docker
PM2
AWS EC2
GitHub Webhooks

⚙️ Workflow
Developer pushes code to GitHub
GitHub webhook triggers Jenkins pipeline
Jenkins:
Clones repository
Builds Docker image
Runs container
Application is deployed on EC2 and accessible via public IP

🎯 Features
Automated CI/CD pipeline
Dockerized Node.js application
Process management using PM2
Real-time deployment on AWS

⚠️ Challenges Faced (Real Issues)
❌ Branch mismatch (master vs main) causing build failure
❌ GitHub webhook not triggering due to incorrect URL / port access
❌ Docker permission denied (/var/run/docker.sock)
❌ Port 3000 already in use (container failed to start)
❌ App not accessible → Node app was not running as a server

✅ Solutions
✔️ Updated branch reference to main
✔️ Fixed webhook URL and opened port 8080 in AWS security group
✔️ Added user to Docker group
✔️ Stopped existing containers before running new ones
✔️ Converted Node app into an HTTP server

📌 Final Outcome
Successfully built a fully automated CI/CD pipeline where every code push triggers deployment on AWS.

## 📸 Screenshots

### Jenkins Pipeline
![Pipeline](screenshots/pipeline.png)

### Docker Container
![Docker](screenshots/webhooks.png)

### Application Output
![App](screenshots/app.png)
