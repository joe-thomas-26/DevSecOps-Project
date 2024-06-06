
# Deploy Netflix Clone on Cloud using Jenkins - DevSecOps Project!

### **Phase 1: Initial Setup and Deployment**

**Step 1: Launch EC2 (Ubuntu 22.04):**

- Provision an EC2 instance on AWS with Ubuntu 22.04.
- Connect to the instance using SSH.

**Step 2: Clone the Code:**

- Update all packages and clone the application code repository onto the EC2 instance.    

**Step 3: Install Docker and Run the App Using a Container:**

- Set up Docker on the EC2 instance:
- Build and run the application using Docker containers

**Step 4: Get the API Key:**

- Obtain a TMDB API key from the TMDB website.
- Recreate the Docker image with the API key

**Phase 2: Security**

1. **Install SonarQube and Trivy:**
    - Install SonarQube and Trivy on the EC2 instance to scan for vulnerabilities.
    - Recreate the Docker image with the API key.      

**Phase 3: CI/CD Setup**

1. **Install Jenkins for Automation:**
    - Install Jenkins on the EC2 instance to automate deployment:
    - Install necessary Jenkins plugins.
    - Configure Java and NodeJS in Global Tool Configuration.
    - Integrate SonarQube with Jenkins and configure the system.
    - Create and configure a Jenkins CI/CD pipeline.
        
2. **Install Dependency-Check and Docker Tools in Jenkins:**

    - Install and configure the Dependency-Check plugin.
    - Install Docker-related plugins and add DockerHub credentials in Jenkins.

**Phase 4: Monitoring**

1. **Install Prometheus and Grafana:**

    - Set up Prometheus for monitoring.
    - Install Node Exporter to collect system-level metrics.
    - Configure Prometheus to scrape metrics from Node Exporter and Jenkins.
    - Install Grafana and set it up to work with Prometheus.
    - Configure Prometheus Plugin Integration:

**Phase 5: Kubernetes**

1. **Create Kubernetes Cluster with Nodegroups:**

    - Set up a Kubernetes cluster with node groups for a scalable environment.
    - Monitor Kubernetes with Prometheus and install Node Exporter using Helm.
    - Add a job to scrape metrics in Prometheus.
    - Deploy Application with ArgoCD:

2. **Install ArgoCD on the Kubernetes cluster.**
    - Set up GitHub repository as a source for ArgoCD.
    - Create and configure an ArgoCD application.
    - Access the application using the appropriate NodeIP and port.

**Phase 7: Cleanup**
1. **Cleanup AWS EC2 Instances:**

    - Terminate AWS EC2 instances that are no longer needed.