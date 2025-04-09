pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/diyadevi21/nodejs-cicd-app.git'
            }
        }

        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test || echo "No test script found"'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-node-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3000:3000 my-node-app'
            }
        }
    }
}
