
pipeline {
    agent any

    environment {
        PATH = "C:\\Users\\Ayush Kasare\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin;${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Getting source code from GitHub'
            }
        }

        stage('Check Docker') {
            steps {
                bat 'docker --version'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-nginx .'
            }
        }

        stage('Verify Docker Image') {
            steps {
                bat 'docker images'
            }
        }
    }
}
