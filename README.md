# 🏓 DevOps Engineer Technical Assignment: Ping-Pong Game Deployment

## 📋 Overview

**🎯 Objective:** Create a production-ready CI/CD pipeline that builds, containerizes, and deploys a Go application to Kubernetes.

---

## 🚀 Application

A Go HTTP server implementing a ping-pong game with these endpoints:

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/ping` | GET | Returns "pong" message |
| `/pong` | GET | Returns "ping" message |
| `/health` | GET | Health check endpoint |
| `/` | GET | API documentation |

**Environment Variables:**
- `PORT` - Server port (default: 8080)
- `SECRET_FILE_PATH` - Path to secret file

**Run Modes:** `server` or `cli`

**Authentication:**
- `Authorization` header with secret token is required for `/ping` and `/pong` endpoints
- in CLI mode, the secret token is passed as a command line argument

**Note:**
- The server will think for 10 seconds before starting the server
- health check endpoint is available at `/health` and it will return 200 OK if the server is ready to serve requests
- The server will be available on the port specified in the `PORT` environment variable
- The server will read the secret token from the `SECRET_FILE_PATH` environment variable
- The secret token is passed as a command line argument in CLI mode

---

## 🎯 Mission

Take this application to production with support for both **x86** and **ARM64** architectures. Have a binary release and a container release available for developers and production.

---

## 📋 Requirements

### 🔒 Security
- [ ] No containers running as root
- [ ] All images must pass security scans
- [ ] No critical/high vulnerabilities should be released to production
- [ ] No secrets in codebase
- [ ] Proper filesystem isolation

### ☸️ Kubernetes
- [ ] Zero-downtime deployments server must be available and ready at all times
- [ ] ARM64 architecture preferred
- [ ] No direct internet access (use ingress/proxy)
- [ ] Cluster can pull from registry

### 🏗️ CI/CD
- [ ] Multi-architecture builds (x86/ARM64)
- [ ] Images stored in GitHub Container Registry
- [ ] Versioned releases with tags
- [ ] Both container and binary releases

---

## 🛠️ Environment

**Prerequisites:**
- Docker
- Minikube or Kind
- kubectl
- Go 1.24
- GitHub account

---

## 📝 Deliverables

- [ ] `Dockerfile`
- [ ] `k8s/` manifests
- [ ] `.github/workflows/` CI/CD pipeline
- [ ] Documentation of your approach

**Note:** Use Minikube/Kind for testing. Be prepared to explain real cloud deployment strategy.

You'll walk us through your work in your technical interview.

---

## 💡 Reminders

- Focus on quality of reasoning over volume.
- Don't make this production-grade; you can do things that don't scale.
- AI tools are welcome. Tell us what you used them for and where they helped or hurt.
- If you hit a wall, write down what you tried and move on.

---

## 🚢 Submission
- Create a fork of this repository and give access to your fork
- Once you notify that you are done no more commits!

---

## ❓ Questions

Have fun! For any question or clarification, reach out without a second thought 🙂

**Echo Team**
