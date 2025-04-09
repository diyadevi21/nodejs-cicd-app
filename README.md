# Node.js CI/CD App using Jenkins

This project demonstrates a simple CI/CD pipeline setup for a Node.js application using Jenkins.

## Project Structure

- node-app-cicd/ – Main application folder
- Jenkinsfile – CI/CD pipeline configuration

## Technologies Used

- Node.js
- Jenkins
- Docker (for containerization)

## Jenkins Pipeline Stages

1. *Install* – Installs Node.js dependencies
2. *Test* – Runs application tests
3. *Build Docker Image* – Builds Docker image from app
4. *Run Container* – Runs the app inside a Docker container

## How to Use

1. Clone this repo
2. Setup Jenkins on your machine
3. Connect this repo as Jenkins project
4. Run the pipeline and observe the stages
5.
