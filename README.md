# DevOps Setup

This is a small Java backend application (though the specifics of what the application does aren't the focus). The main emphasis of this project is to demonstrate how various DevOps tools and technologies can be utilized to automate infrastructure provisioning, continuous integration, and deployment pipelines.

The project was built as part of a DevOps learning process.

## Tools and Technologies Used:
This project makes extensive use of popular DevOps tools and practices. Below is a breakdown of the key tools used:

### 1. **Terraform**
   - **Purpose**: Infrastructure as Code (IaC) tool used to provision and manage cloud resources.
   - **Usage**: 
     - Set up AWS infrastructure, including creating a Virtual Private Cloud (VPC) and an Elastic Kubernetes Service (EKS) cluster.
     - Automates provisioning of Jenkins servers and other resources.
   - **Key Features**: 
     - Writing Terraform files to create EC2 instances, VPCs, and EKS clusters.
     - Managing infrastructure state and ensuring repeatability.

### 2. **Ansible**
   - **Purpose**: Configuration management and automation tool.
   - **Usage**: 
     - Configure Jenkins master and slave nodes.
     - Install necessary packages like Maven and Docker on the servers.
     - Automate the setup of Jenkins pipelines, Maven builds, and Docker configurations.
   - **Key Features**: 
     - Writing and running Ansible playbooks to automate server configurations.

### 3. **Jenkins**
   - **Purpose**: Continuous Integration/Continuous Deployment (CI/CD) tool.
   - **Usage**: 
     - Set up Jenkins as a CI server to automate build, test, and deployment pipelines.
     - Use multibranch pipelines and GitHub webhooks to automatically trigger jobs on code changes.
     - Integrate Jenkins with other tools like SonarQube and Docker.
   - **Key Features**: 
     - Jenkins pipelines, multibranch pipelines, GitHub integration, and webhooks.

### 4. **Maven**
   - **Purpose**: Build automation tool for Java projects.
   - **Usage**: 
     - Maven is used in the Jenkins pipelines to handle the build process for the Java application.
     - Automate the compilation, testing, and packaging of the Java application.

### 5. **SonarQube**
   - **Purpose**: Continuous code quality and security analysis.
   - **Usage**: 
     - Integrated into Jenkins pipelines to analyze code quality and ensure best practices are followed.
     - Configured SonarQube rules and quality gates to monitor code health.

### 6. **JFrog Artifactory**
   - **Purpose**: Artifact repository manager.
   - **Usage**: 
     - Store build artifacts such as JAR files and Docker images.
     - Jenkins pipelines are configured to push the built artifacts to Artifactory.

### 7. **Docker**
   - **Purpose**: Containerization platform.
   - **Usage**: 
     - Docker is used to create containers for the application and other services like Jenkins agents.
     - Automated Docker image creation and deployment to Artifactory.
   
### 8. **Kubernetes**
   - **Purpose**: Container orchestration platform.
   - **Usage**: 
     - Deploy the Java application and other services on AWS EKS (Kubernetes).
     - Use Helm charts to automate Kubernetes deployments.
   
### 9. **Helm**
   - **Purpose**: Kubernetes package manager.
   - **Usage**: 
     - Helm charts are used to package Kubernetes applications and deploy them to the cluster efficiently.
     - Manage deployments of Jenkins, the Java app, and other services via Helm.

### 10. **Prometheus & Grafana**
   - **Purpose**: Monitoring and visualization tools.
   - **Usage**: 
     - Monitor the performance and health of the Kubernetes cluster and other resources.
     - Set up dashboards in Grafana to visualize metrics collected by Prometheus.

## Key Features of the CI/CD Pipeline:
- **Infrastructure as Code**: Use Terraform to automate the provisioning of AWS resources like EC2 instances and EKS clusters.
- **Configuration Management**: Use Ansible to manage server configurations and install necessary tools like Maven, Jenkins, and Docker.
- **Continuous Integration**: Jenkins is used to automatically build, test, and analyze code quality on every commit.
- **Continuous Deployment**: Automate the deployment of Dockerized applications to Kubernetes clusters using Helm.
- **Code Quality**: Integrate SonarQube to ensure code quality and enforce security best practices.
- **Artifact Management**: Store and manage build artifacts and Docker images in JFrog Artifactory.
- **Monitoring**: Use Prometheus and Grafana to monitor the health of the Kubernetes cluster and set up performance dashboards.
