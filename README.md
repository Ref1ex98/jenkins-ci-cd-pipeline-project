# Jenkins CI/CD Pipeline Project

## Project Overview

This project demonstrates a complete CI/CD pipeline implementation using Jenkins, AWS EC2, GitHub Webhooks, and Jenkins Master-Agent architecture.

The pipeline automates:
- Source code integration
- Automated build triggering
- Test environment deployment
- Production environment deployment
- Multi-node Jenkins execution

---

# Technologies Used

- Jenkins
- AWS EC2
- Ubuntu 24.04
- Git & GitHub
- GitHub Webhooks
- Linux Shell Scripting
- OpenJDK 21

---

# Jenkins Architecture

```text
                           +-------------------+
                           |   Developer PC    |
                           | (VS Code + Git)   |
                           +---------+---------+
                                     |
                                     | git push
                                     v
                        +--------------------------+
                        |        GitHub Repo       |
                        | develop / test / main    |
                        +------------+-------------+
                                     |
                                     | Webhook Trigger
                                     v
                     +--------------------------------+
                     |       Jenkins Master Node      |
                     |        (EC2 Ubuntu)            |
                     +---------------+----------------+
                                     |
                 -----------------------------------------
                 |                                       |
                 |                                       |
                 v                                       v

      +------------------------+            +------------------------+
      |   Test Agent Node      |            |   Prod Agent Node      |
      |    (EC2 Ubuntu)        |            |    (EC2 Ubuntu)        |
      +-----------+------------+            +-----------+------------+
                  |                                         |
                  | Deploy Test Build                       | Deploy Production Build
                  v                                         v

      +------------------------+            +------------------------+
      |  /test-deployment      |            |  /prod-deployment      |
      +------------------------+            +------------------------+
```

---

# Assignment 1 - Jenkins Webhook Automation

## Workflow

```text
GitHub Push (develop branch)
            ↓
GitHub Webhook Trigger
            ↓
Jenkins Job Execution
            ↓
Deployment on slave1 node
```

## Features Implemented

- Jenkins Master-Agent setup
- GitHub Webhook integration
- Automatic Jenkins job triggering
- Deployment automation on Jenkins agent

---

# Assignment 2 - Branch Based Deployment

## Workflow

### Test Environment

```text
Push to test branch
        ↓
Push-to-Test Job
        ↓
Deployment on Test Node
```

### Production Environment

```text
Push to main branch
        ↓
Push-to-Prod Job
        ↓
Deployment on Production Node
```

## Features Implemented

- Separate deployment environments
- Branch-based CI/CD logic
- Automated deployment to different servers
- Multi-node Jenkins architecture

---

# Assignment 3 - CI/CD Pipeline Chaining

## Workflow

```text
Push to develop branch
          ↓
Pipeline-Test Job
          ↓
Deploy to Test Node
          ↓
Pipeline-Prod Job
          ↓
Deploy to Production Node
```

## Features Implemented

- Jenkins Build Pipeline Plugin
- Automated pipeline chaining
- Test to Production promotion flow
- End-to-end CI/CD automation

---

# Project Structure

```text
jenkins-ci-cd-pipeline-project/
│
├── app/
│   └── index.html
│
├── notes/
│
├── scripts/
│   ├── install-java.sh
│   └── install-jenkins.sh
│
├── screenshots/
│   ├── assignment1/
│   ├── assignment2/
│   └── assignment3/
│
├── README.md
└── .gitignore
```

---

# Jenkins Nodes Used

| Node Name | Purpose |
|------------|----------|
| master     | Jenkins Controller |
| slave1     | Assignment 1 Deployment |
| test       | Test Environment |
| prod       | Production Environment |

---

# Screenshots

Project screenshots are available inside the `screenshots/` directory.

Screenshots include:
- Jenkins Dashboard
- Jenkins Nodes
- Successful Build History
- Pipeline View
- GitHub Webhook Deliveries
- AWS EC2 Instances
- Deployment Verification

---

# Key Learning Outcomes

- Jenkins Master-Agent Architecture
- GitHub Webhook Integration
- Multi-node Jenkins Configuration
- Branch-based Deployment
- Automated CI/CD Pipelines
- AWS EC2 Management
- Linux Server Administration
- Jenkins Freestyle Jobs
- Build Pipeline Automation

---

# Future Improvements

- Docker Integration
- Jenkinsfile Pipelines
- Terraform Infrastructure Automation
- Nginx Reverse Proxy
- Monitoring & Logging
- Kubernetes Deployment

---

# Author

Rohan Surwade

