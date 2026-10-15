pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t python-cicd-app:latest .'
            }
        }

        stage('Test Python Application') {
            steps {
                sh 'python3 --version'
                sh 'docker image inspect python-cicd-app:latest'
            }
        }
    }
}
