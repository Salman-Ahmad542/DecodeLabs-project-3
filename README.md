# DecodeLabs Project 3 — CI/CD Pipeline

## 📌 Project Overview

This project demonstrates the implementation of a basic **CI/CD (Continuous Integration and Continuous Deployment) pipeline** for a responsive website using **GitHub and Jenkins**.

The purpose of this project is to automate the process of taking source code from a GitHub repository, building and validating the project, testing the required files, and completing the deployment stage through Jenkins.

The pipeline is divided into four stages:

```text
GitHub
   ↓
Jenkins
   ↓
Checkout
   ↓
Build
   ↓
Test
   ↓
Deploy
```

---

## 🎯 Project Objectives

The main objectives of this project are:

* Understand the basic concept of CI/CD.
* Learn how to integrate GitHub with Jenkins.
* Create a Jenkins Pipeline using a `Jenkinsfile`.
* Automate the project build process.
* Perform basic automated testing.
* Create multiple Jenkins pipeline stages.
* Monitor pipeline execution using Jenkins Stage View.
* Understand the basic workflow of automated software delivery.

---

## 🛠️ Technologies and Tools

The following technologies and tools were used:

| Technology / Tool | Purpose                            |
| ----------------- | ---------------------------------- |
| HTML              | Website structure                  |
| CSS               | Website styling                    |
| Git               | Version control                    |
| GitHub            | Source code repository             |
| Jenkins           | CI/CD automation                   |
| Jenkins Pipeline  | Automated workflow                 |
| Linux             | Development and server environment |
| Bash/Shell        | Command-line operations            |

---

## 📁 Project Structure

```text
DecodeLabs-Project-3-CICD-Website/
│
├── index.html
├── style.css
├── Jenkinsfile
└── README.md
```

### File Description

### `index.html`

Contains the main structure and content of the website.

### `style.css`

Contains the styling and visual design of the website.

### `Jenkinsfile`

Contains the Jenkins Pipeline configuration used to automate the CI/CD workflow.

### `README.md`

Contains the documentation and explanation of the project.

---

# 🔄 CI/CD Pipeline Workflow

The project uses Jenkins to automate the following workflow:

```text
Developer
    ↓
Git
    ↓
GitHub Repository
    ↓
Jenkins
    ↓
Checkout
    ↓
Build
    ↓
Test
    ↓
Deploy
    ↓
Successful Pipeline
```

Whenever Jenkins runs the pipeline, it processes the project through the configured stages.

---

# 🚀 Jenkins Pipeline Stages

The Jenkins pipeline contains four stages.

## 1. Checkout

The **Checkout** stage retrieves the source code from the GitHub repository.

Repository:

```text
https://github.com/Salman-Ahmad542/DecodeLabs-project-3.git
```

This allows Jenkins to work with the latest project files stored in GitHub.

---

## 2. Build

The **Build** stage checks that the required website files are available.

The pipeline verifies:

```text
index.html
style.css
```

If the required files exist, the build stage completes successfully.

---

## 3. Test

The **Test** stage performs basic validation of the website project.

It checks that the expected project content exists in the HTML file.

If the validation passes, Jenkins continues to the deployment stage.

---

## 4. Deploy

The **Deploy** stage represents the deployment step of the CI/CD workflow.

After the build and test stages complete successfully, Jenkins executes the deployment stage.

---

# 📜 Jenkinsfile

The pipeline is defined inside the `Jenkinsfile`.

The basic pipeline structure is:

```groovy
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Project 3...'
                sh 'test -f index.html'
                sh 'test -f style.css'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing website files...'
                sh 'grep -q "CI/CD Pipeline Basics" index.html'
                echo 'All tests passed.'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying website...'
            }
        }
    }
}
```

---

# 🔗 GitHub Integration

The project source code is hosted on GitHub.

**GitHub Repository:**

```text
https://github.com/Salman-Ahmad542/DecodeLabs-project-3.git
```

The repository contains the website files and Jenkins pipeline configuration.

---

# ⚙️ Jenkins Configuration

A Jenkins Pipeline job was created for the project.

The Jenkins job uses:

```text
Definition: Pipeline script from SCM
SCM: Git
Branch: */main
Script Path: Jenkinsfile
```

Jenkins retrieves the `Jenkinsfile` from the GitHub repository and executes the defined pipeline.

---

# 📊 Pipeline Stage View

Jenkins Stage View was used to monitor the pipeline execution.

The completed pipeline showed:

```text
Checkout    Build    Test    Deploy
   ✓          ✓       ✓        ✓
```

All four stages completed successfully.

---

# 🧪 Testing and Verification

The CI/CD pipeline was tested through Jenkins.

The following stages were successfully verified:

| Stage    | Status       |
| -------- | ------------ |
| Checkout | ✅ Successful |
| Build    | ✅ Successful |
| Test     | ✅ Successful |
| Deploy   | ✅ Successful |

The Jenkins Stage View confirmed that the complete pipeline executed successfully.

---

# 🌐 Website

The final website was opened and verified through a web browser after completing the project deployment process.

The website provides the final visual output of the project and confirms that the web files are working correctly.

---

# 📚 Learning Outcomes

This project provided practical experience with:

* CI/CD fundamentals
* Git and GitHub
* Jenkins
* Jenkins Pipeline
* Jenkinsfile
* GitHub and Jenkins integration
* Automated build validation
* Basic automated testing
* Pipeline stages
* Jenkins Stage View
* Linux command-line operations
* Basic deployment workflow

---

# 🏆 Final Result

The CI/CD pipeline was successfully created, configured, executed, and verified.

Final pipeline:

```text
Checkout → Build → Test → Deploy
```

All stages completed successfully.

**Project Status: COMPLETED & VERIFIED ✅**

---

## 👨‍💻 Project Information

**Project:** DecodeLabs Project 3
**Title:** CI/CD Pipeline
**Domain:** DevOps Engineering
**Batch:** 2026
**Status:** Completed & Verified
