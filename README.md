# Node.js Docker CI/CD Pipeline

## 📌 Project Overview

This project demonstrates a basic **CI/CD pipeline for a Node.js application** using **Docker, GitHub Actions, and Docker Hub**.

The application is containerized using Docker, and GitHub Actions is configured to automatically build and push the Docker image to Docker Hub whenever changes are pushed to the `main` branch.

---

## 🛠️ Technologies Used

* Node.js
* Docker
* Docker Hub
* Git & GitHub
* GitHub Actions
* GitHub Secrets
* PowerShell

---

## 📁 Project Structure

```text
nodejs-demo-app/
│
├── .github/
│   └── workflows/
│       └── ci-cd.yml
│
├── index.html
├── index.js
├── package.json
├── package-lock.json
├── Dockerfile
├── .dockerignore
├── .gitignore
├── cicd-test.txt
└── README.md
```

---

## 🚀 Application Setup

The Node.js application runs on port `5000`.

### Install dependencies

```bash
npm install
```

### Run the application

```bash
node index.js
```

The application can then be accessed at:

```text
http://localhost:5000
```

---

## 🐳 Docker Setup

A `Dockerfile` is used to containerize the application.

### Build Docker image

```bash
docker build -t nodejs-demo-app .
```

### Run Docker container

```bash
docker run -p 5000:5000 nodejs-demo-app
```

The application can then be accessed at:

```text
http://localhost:5000
```

---

## 🔄 CI/CD Pipeline

GitHub Actions is used to automate the Docker image build and push process.

The workflow is stored at:

```text
.github/workflows/ci-cd.yml
```

### Pipeline Flow

```text
Developer makes code change
          ↓
     git push main
          ↓
   GitHub Actions Trigger
          ↓
      Checkout Code
          ↓
   Login to Docker Hub
          ↓
    Build Docker Image
          ↓
    Push Image to Docker Hub
```

---

## 🔐 GitHub Secrets

Docker Hub credentials are stored securely using **GitHub Repository Secrets**.

The following secrets are used:

```text
DOCKERHUB_USERNAME
DOCKERHUB_TOKEN
```

`DOCKERHUB_USERNAME` contains the Docker Hub username.

`DOCKERHUB_TOKEN` contains a Docker Hub Personal Access Token.

> The actual token is not stored in the repository or committed to GitHub.

---

## 🐋 Docker Hub Image

The Docker image is published to Docker Hub using the following repository:

```text
bhumika015/nodejs-demo-app
```

The image is tagged as:

```text
latest
```

---

## 🧪 CI/CD Trigger Test

To verify that the pipeline works automatically, a code/file change was made and pushed to the `main` branch.

Example:

```text
cicd-test.txt
```

After the change was pushed, GitHub Actions automatically started the workflow.

---

## 📸 Screenshots

Screenshots related to the task can be added to the repository if required.

Suggested screenshots:

1. Node.js application running locally
2. Docker image build
3. Docker container running
4. Docker Hub repository
5. GitHub Actions workflow
6. Successful build/push workflow

---

## 📚 What I Learned

Through this task, I learned how to:

* Create and run a Node.js application.
* Create a Dockerfile.
* Build a Docker image.
* Run an application inside a Docker container.
* Push Docker images to Docker Hub.
* Create a GitHub Actions workflow.
* Configure GitHub Repository Secrets.
* Trigger CI/CD automatically using Git pushes.
* Automate Docker image building and publishing.

---

## 👩‍💻 Author

**Bhumika Tiwari**

B.Tech Computer Science Engineering Graduate

Interested in:

* AWS Cloud
* DevOps
* Docker
* Kubernetes
* Terraform
* CI/CD
* Cloud Infrastructure

