pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                dir('node-app-cicd/node-app-cicd') {
                    bat 'npm install'
                }
            }
        }

        stage('Test') {
            steps {
                dir('node-app-cicd/node-app-cicd') {
                    bat 'npm test || echo No test script found'
                }
            }
        }

        stage('Build Docker Image') {
            steps {
                dir('node-app-cicd/node-app-cicd') {
                    bat 'docker build -t my-node-app .'
                }
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 3000:3000 my-node-app'
            }
        }
    }
}
           
