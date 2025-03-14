pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Varu-k/PES1UG23CS842_Jenkins..git'
            }
        }
        stage('Build application') {
            steps {
                sh 'g++ -o PES1UG23CS842-1 main.cpp'
            }
        }
        stage('Test application') {
            steps {
                sh './PES1UG23CS842-1'
            }
        }
        stage('Deploy application') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
    }
}
