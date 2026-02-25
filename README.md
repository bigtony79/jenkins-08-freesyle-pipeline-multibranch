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
6. Click "Apply" and "Save"
![alt text](images/image2.png)

### Install Node.js and npm
1. Log into the Jenkins container as root by running the following command

``` 
docker exec -it -u 0 <container ID or name> bash
```
2. Update the package list and install Node.js and npm by running the following commands:

```
apt update
apt install -y nodejs npm
```
3. Verify node.js and npm packages are installed

```
node -v
npm -v
```


## Create Freestyle job
1. Click create "Create a job"
2. Enter a name for job. For example, you can enter "my-freestyle-job"
3. Select "Freestyle project" and click "Ok" button <img width="344" height="19" alt="image" src="https://github.com/user-attachments/assets/db294dd4-bcdb-4aaf-b691-4e5cbd1b94c8" />




