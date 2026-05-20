# AWS Jenkins CI/CD Project

This project demonstrates a CI/CD pipeline using AWS EC2, Jenkins master-agent architecture, GitHub webhooks, and automated deployments.

---

## Technologies Used

- AWS EC2
- Jenkins
- GitHub
- Linux
- CI/CD
- Webhooks

---

## Architecture

```text
GitHub
   |
   v
Jenkins Master
   |
   v
Jenkins Agent (slave1)
```

---

## Workflow

```text
Git Push → GitHub Webhook → Jenkins Job → Agent Deployment
```

---

## Features

- Automated Jenkins builds
- GitHub webhook integration
- Jenkins master-agent setup
- Branch-based CI/CD workflow

---

## Author

Rohan
