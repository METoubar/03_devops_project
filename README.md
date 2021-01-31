# 03_devops_project
This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

The repository contains a simple Node.js and React application which generates a web page with the content "Welcome to React" and is accompanied by a test to check that the application renders satisfactorily.

## Jenkins CI/CD

Using jenkins as a CI/CD tool that run the docker-compose file which is responsible for creating the containers for build and test, and the communication between them.

After creating the Jenkins pipeline, making a change in the code,
Make a new pull request to trigger and merge the changes.

Configuring Slack notification plugin in Jenkins, and calling it in the Jenkinsfile to send pipeine status notification.

## Nexus

Nexus could be used as an artifact repository tool, forstoring build and test outputs.