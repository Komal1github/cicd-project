pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git branch: 'master', url: 'https://github.com/Komal1github/cicd-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t cicd-app .'   // use 'sh' if Linux
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run cicd-app'
            }
        }
    }
}