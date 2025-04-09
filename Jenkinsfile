 pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                bat 'npm test'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-nodejs-app .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 3000:3000 my-nodejs-app'
            }
        }
    }
} 
