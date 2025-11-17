# teraform-project
# DevOps CI/CD Pipeline Project

## Overview
This project demonstrates a full CI/CD pipeline using Jenkins, integrated with GitHub, Docker, Terraform, SonarQube, OWASP Dependency Check, and deployment to Tomcat on AWS. It builds a sample web app (vprofile-v2.war), scans for vulnerabilities, pushes Docker images to DockerHub, and deploys to a Tomcat server.

Key Technologies:
- **CI/CD:** Jenkins Pipeline
- **IaC:** Terraform (S3 backend for state)
- **Containerization:** Docker
- **Security:** OWASP, Trivy scans
- **Code Quality:** SonarQube, Maven
- **Storage:** AWS S3 for artifacts
- **Deployment:** Tomcat 9

## Screenshots
<img width="1920" height="1080" alt="tomcat-home" src="https://github.com/user-attachments/assets/a77f9690-aad5-4a39-97b4-d1b3dfcfaeb1" />
<img width="1900" height="802" alt="Full-deploy" src="https://github.com/user-attachments/assets/4e0fe333-df4b-46c1-846c-f4bb3f77f9bb" />
<img width="1904" height="876" alt="dockerhub-images" src="https://github.com/user-attachments/assets/e61806d4-42b5-4bea-ba3c-c2bb8e305671" />
<img width="1920" height="872" alt="live-page" src="https://github.com/user-attachments/assets/e30c6493-3c1c-4d34-90fc-702e10520dc9" />


## Setup Instructions
1. Clone the repo: `git clone https://github.com/yourusername/my-devops-cicd-project.git`
2. Install dependencies (Maven, Docker, Terraform).
3. Set up Jenkins with required plugins (e.g., SonarQube, OWASP, S3).
4. Configure credentials (use Jenkins Credentials for secrets).
5. Run `terraform init` in `/terraform/` to set up S3 backend.
6. Trigger build in Jenkins.

## Pipeline Stages
- CleanWS
- Code Checkout (from GitHub)
- CQA (SonarQube)
- Code Build (Maven)
- OWASP Scan
- Artifact Upload (S3)
- Image Build (Docker)
- Trivy Scan
- Tag & Push (DockerHub)
- Deploy (Tomcat)

## Prerequisites
- AWS Account (S3 bucket: amazn-s3-bucket-ksn)
- DockerHub Account
- Tomcat Server (e.g., at http://44.192.31.210:8080)

Feel free to fork and contribute!
