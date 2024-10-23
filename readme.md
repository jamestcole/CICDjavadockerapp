# CICD Java Docker Application

This project is a simple Java application integrated with a CI/CD pipeline using Jenkins and Docker. Each push to the repository triggers an automatic build and test process through Jenkins.

## Features

- Java application packaged using Docker.
- Continuous Integration (CI) with Jenkins.
- Automatically triggered builds and tests on every code push.
- GitHub Webhook for automated Jenkins job triggers.

## Prerequisites

Make sure you have the following installed:

- [Java](https://www.oracle.com/java/technologies/javase-downloads.html)
- [Maven](https://maven.apache.org/install.html)
- [Docker](https://docs.docker.com/get-docker/)
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Jenkins](https://www.jenkins.io/doc/book/installing/)

### Jenkins Setup

1. Install Jenkins on your machine or server.
2. Make sure you have the following plugins installed on Jenkins:
   - **GitHub Integration Plugin**
   - **Pipeline Plugin**
   - **Docker Plugin** (optional if you're using Docker in the pipeline)

### GitHub Webhook Setup

1. Go to your GitHub repository: [CICDjavadockerapp](https://github.com/jamestcole/CICDjavadockerapp).
2. Navigate to **Settings > Webhooks**.
3. Click **Add Webhook**.
4. Set the Payload URL to your Jenkins server’s GitHub Webhook URL:
   ```bash
   http://<YOUR-JENKINS-SERVER-URL>/github-webhook/