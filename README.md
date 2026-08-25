# jenkins-cicd-demo1
Jenkins CI/CD & GitHub Integration

📌 Project Overview

This project demonstrates a basic CI/CD pipeline using Jenkins and GitHub.

The objective is to understand how source code moves from a GitHub repository through Jenkins, where automated checkout, build, and testing stages are performed.

🛠️ Technologies Used

* Jenkins
* Git
* GitHub
* Jenkinsfile
* CI/CD
* Linux
* Bash
* HTML

📂 Project Structure

jenkins-cicd-project/
│
├── Jenkinsfile
├── index.html
└── README.md

🔄 CI/CD Pipeline Flow

Developer
    ↓
GitHub Repository
    ↓
GitHub Webhook
    ↓
Jenkins
    ↓
Checkout
    ↓
Build
    ↓
Test
    ↓
Pipeline Result

🚀 Pipeline Stages

1. Checkout

Jenkins retrieves the latest source code from the GitHub repository.

2. Build

Jenkins verifies the project files and performs the build-related commands.

3. Test

Jenkins checks whether the required application file exists and validates the project.

📄 Jenkinsfile

The project uses a Declarative Jenkins Pipeline.

pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building application...'
                sh 'ls -la'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing application...'
                sh 'test -f index.html'
            }
        }
    }
    post {
        success {
            echo 'CI/CD Pipeline Successful'
        }
        failure {
            echo 'CI/CD Pipeline Failed'
        }
    }
}

🔐 Jenkins Credentials

GitHub authentication is configured using Jenkins Credentials.

Sensitive information such as GitHub passwords or Personal Access Tokens should not be stored directly inside the Jenkinsfile.

🔗 GitHub Webhook

A GitHub Webhook can be configured to notify Jenkins whenever code is pushed to the repository.

Git Push
   ↓
GitHub
   ↓
Webhook
   ↓
Jenkins
   ↓
Pipeline Automatically Starts

🧪 Pipeline Testing

The pipeline is tested by executing the following stages:

* Checkout
* Build
* Test

A successful execution should display:

Checkout     SUCCESS
Build        SUCCESS
Test         SUCCESS

🔧 Troubleshooting

Common Jenkins pipeline issues include:

* Incorrect GitHub repository URL
* Invalid GitHub credentials
* Incorrect branch name
* Jenkinsfile syntax errors
* Missing files
* GitHub Webhook configuration problems
* Jenkins service not running

Build failures can be investigated using:

Jenkins → Build → Console Output

🎯 Learning Objectives

Through this project, the following concepts are practiced:

* Jenkins fundamentals and architecture
* Jenkins installation and configuration
* Jenkins jobs and builds
* Jenkins Credentials
* GitHub integration
* Freestyle projects
* Declarative Pipelines
* Jenkinsfile
* Pipeline stages
* Build triggers
* GitHub Webhooks
* Build and test automation
* Pipeline troubleshooting
* CI/CD best practices

👨‍💻 Author

Saif Rahman Shaik

DevOps Engineer

📌 Project Purpose

This project was created as part of a DevOps/Jenkins CI/CD hands-on assignment to demonstrate practical Jenkins and GitHub integration.
