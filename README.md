# Brain Tasks DevOps Project

## Project Overview

This project demonstrates a complete DevOps workflow using Docker, Amazon ECR, Amazon EKS, AWS CodeBuild, AWS CodePipeline, and CloudWatch.

The application was deployed to Kubernetes running on Amazon EKS and automated through a CI/CD pipeline.

---

## Architecture

GitHub Repository
↓
CodePipeline
↓
CodeBuild
↓
Amazon ECR
↓
Amazon EKS
↓
AWS LoadBalancer
↓
Application Access

---

## Technologies Used

* GitHub
* Docker
* Amazon ECR
* Amazon EKS
* Kubernetes
* AWS CodeBuild
* AWS CodePipeline
* Amazon CloudWatch

---

## Application Repository

GitHub Repository:

https://github.com/Radha96dev/Brain-Tasks-App

---

## Docker Implementation

### Build Docker Image

```bash
docker build -t brain-tasks-app .
```

### Run Docker Container

```bash
docker run -d -p 3000:80 --name brain-tasks-app brain-tasks-app
```

---

## Amazon ECR

### Create Repository

```bash
aws ecr create-repository --repository-name brain-tasks-app
```

### Push Image

```bash
docker push <ECR_IMAGE_URI>
```

---

## Kubernetes Deployment

### Deployment

deployment.yaml created with 2 replicas.

### Service

service.yaml created with LoadBalancer type.

### Deploy Application

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

### Verify

```bash
kubectl get deployments
kubectl get pods
kubectl get svc
```

---

## EKS Cluster

Cluster Name:

brain-cluster

---

## CI/CD Pipeline

### Source Stage

GitHub Repository

### Build Stage

AWS CodeBuild

### Deploy Stage

Amazon EKS

Pipeline Flow:

GitHub → CodeBuild → Amazon EKS

---

## Monitoring

Amazon CloudWatch Logs used for:

* CodeBuild Logs
* CodePipeline Logs

Log Groups:

* /aws/codebuild/brain-tasks-build
* /aws/codepipeline/brain-tasks-pipeline

---

## LoadBalancer Endpoint

Replace with your current LoadBalancer DNS:

aff53387fdb4b4f3ba0d5269c3d7bfb5-891360583.ap-south-1.elb.amazonaws.com

---

## Screenshots

Include screenshots for:

1. GitHub Repository
2. Docker Build
3. ECR Repository
4. EKS Cluster
5. Kubernetes Pods
6. Kubernetes Service
7. LoadBalancer Access
8. CodeBuild Success
9. CodePipeline Success
10. CloudWatch Logs

---

## Project Status

Project Completed Successfully.
