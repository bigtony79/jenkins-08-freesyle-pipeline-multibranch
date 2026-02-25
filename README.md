# Demo Project - Create CI Pipeline (Freestyle, Pipeline, Multibranch Pipeline)

## Overview
Install build tools in Jenkins and create CI pipelines using chained freestyle jobs, a pipeline and a multibranch pipeline.

## Technologies used: 
Jenkins, Docker, Linux, Git, Java, Maven 

## Project Description: 
CI Pipeline for a Java Maven application to build and push to the repository 
* Install Build Tools (Maven, Node) in Jenkins
* Make Docker available on Jenkins server
* Create Jenkins credentials for a git repository
* Create different Jenkins job types (Freestyle, Pipeline, Multibranch pipeline) for the Java Maven project with Jenkinsfile to:
  - Connect to the application’s git repository
  - Build JAR
  - Build Docker Image
  - Push to private DockerHub repository

## Install Build Tools 
### Install Maven
1. Log into Jenkins and go to "Manage Jenkins" by clicking on the Gear icon on the top right
2. Click on Tools 
![alt text](images/maven-build.png)
3. Scroll down and Click on "+ Add Maven" button 
4. In the Name field, enter a value such as "maven-3.9"
5. Select the desired version under "Install from Apache" block
6. Click "Apply" and "Save" buttons.
![alt text](images/image2.png)

### Install Node.js and npm
1. Log into the Jenkins container as root by running the following command as 

```docker exec -it -u 0 <container ID or name> bash
```


## Configure Docker to be available on the Jenkins server
## 
