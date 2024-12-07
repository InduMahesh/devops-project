pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/InduMahesh/https://github.com/InduMahesh/devops-project.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t bmi-calculator .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker stop bmi-calculator || true && docker rm bmi-calculator || true'
                sh 'docker run -d --name bmi-calculator -p 8085:80 bmi-calculator'
            }
        }
    }
