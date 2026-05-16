# 🚀 End-to-End CI/CD Pipeline Project using Jenkins, Maven, Tomcat & Azure

## 📌 Project Overview

This project demonstrates a complete **CI/CD (Continuous Integration & Continuous Deployment)** pipeline for deploying a Java web application using:

* GitHub
* Jenkins
* Maven
* Apache Tomcat
* Azure Virtual Machines
* Ubuntu Linux

The project automates:

✅ Pulling source code from GitHub
✅ Building Java application using Maven
✅ Creating WAR file
✅ Deploying application to Apache Tomcat
✅ Hosting application publicly on Azure VM

---

# 🏗️ Project Architecture

```text
Developer
   ↓
GitHub Repository
   ↓
Jenkins CI/CD Pipeline
   ↓
Maven Build Process
   ↓
WAR File Generation
   ↓
Apache Tomcat Deployment
   ↓
Live Web Application
```

---

# 🛠️ Technologies Used

| Technology    | Purpose                |
| ------------- | ---------------------- |
| Azure VM      | Cloud Infrastructure   |
| Ubuntu Linux  | Operating System       |
| GitHub        | Source Code Management |
| Jenkins       | CI/CD Automation       |
| Maven         | Build Tool             |
| Apache Tomcat | Application Server     |
| Java 17       | Runtime Environment    |
| Git           | Version Control        |

---

# ☁️ Infrastructure Setup

## 🔹 Jenkins Server

Purpose:

* Build automation
* CI/CD execution
* WAR generation

Installed:

* Jenkins
* Java 17
* Maven
* Git

---

## 🔹 Tomcat Server

Purpose:

* Deploy and host Java application

Installed:

* Apache Tomcat 10
* Java 17

---

# ⚙️ Jenkins Installation

## Install Java

```bash
sudo apt update
sudo apt install openjdk-17-jdk -y
```

## Add Jenkins Repository

```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
/usr/share/keyrings/jenkins-keyring.asc > /dev/null
```

```bash
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null
```

## Install Jenkins

```bash
sudo apt update
sudo apt install jenkins -y
```

## Start Jenkins

```bash
sudo systemctl enable jenkins
sudo systemctl start jenkins
```

---

# 🐱 Apache Tomcat Setup

## Download Tomcat

```bash
wget https://archive.apache.org/dist/tomcat/tomcat-10/v10.1.42/bin/apache-tomcat-10.1.42.tar.gz
```

## Extract Tomcat

```bash
sudo mkdir -p /opt/tomcat
sudo tar -xzf apache-tomcat-10.1.42.tar.gz -C /opt/tomcat --strip-components=1
```

## Start Tomcat

```bash
cd /opt/tomcat/bin
./startup.sh
```

---

# 🔗 GitHub Integration

GitHub Repository:

```text
https://github.com/saishekar555/jenkins
```

Jenkins pulls the latest source code directly from GitHub.

---

# 📦 Maven Build Process

## Build Command

```bash
mvn clean package
```

Generated Artifact:

```text
MyWebApp.war
```

---

# 🚀 Deployment Process

```text
Code Change → GitHub → Jenkins Build → WAR File → Tomcat Deployment → Live Website
```

---

# 📋 Jenkins Job Configuration

## Source Code Management

* Git Repository configured
* Main branch connected

## Build Step

```bash
mvn -f MyWebApp/pom.xml clean package
```

## Post Build Action

* Deploy WAR/EAR to Tomcat Container
* Automatic deployment enabled

---

# 🌐 Live Application

```text
http://<TOMCAT-IP>:8080/jenkins/
```

---

# ⚠️ Challenges Faced

## Issue 1 — Jenkins Not Starting

### Fix:

Installed Java 17 correctly and restarted Jenkins.

---

## Issue 2 — Tomcat 403 Access Denied

### Fix:

Modified Tomcat context.xml file to allow remote access.

---

## Issue 3 — Azure Port Access Issue

### Fix:

Added inbound rule for TCP port 8080 in Azure NSG.

---

## Issue 4 — Tomcat Service Failure

### Fix:

Updated JAVA_HOME path in tomcat.service file.

---

# 📚 DevOps Concepts Learned

* Continuous Integration (CI)
* Continuous Deployment (CD)
* Linux Administration
* Cloud Infrastructure Management
* Build Automation
* Deployment Automation
* Git Workflow
* Java Application Deployment

---

# 📄 Resume Description

Designed and implemented an end-to-end CI/CD pipeline using Jenkins, Maven, GitHub, Apache Tomcat, and Azure Virtual Machines for automated Java web application deployment. Configured Jenkins jobs for automated build and deployment, integrated GitHub for source control, deployed WAR artifacts to Tomcat servers, and managed Linux-based cloud infrastructure on Azure.

---

# 🎯 Future Enhancements

* Docker Integration
* Kubernetes Deployment
* Jenkins Pipeline as Code
* GitHub Webhooks
* Terraform Automation
* Azure DevOps Pipelines
* Monitoring with Grafana & Prometheus

---

# ✅ Project Outcome

Successfully implemented:

✅ Automated CI/CD pipeline
✅ Jenkins-Tomcat integration
✅ Maven automated build process
✅ GitHub source integration
✅ Public Java application hosting on Azure

---

# 👨‍💻 Author

**Dammoju Sai Shekar Chary**

DevOps & Cloud Enthusiast

