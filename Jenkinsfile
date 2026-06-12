pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t portfolio-app .'
            }
        }

        stage('Deploy Container') {
            steps {
                bat '''
                docker stop portfolio-container >nul 2>&1
                docker rm portfolio-container >nul 2>&1
                docker run -d --name portfolio-container -p 8080:80 portfolio-app
                '''
            }
        }

        stage('Verify Deployment') {
            steps {
                bat 'docker ps'
            }
        }

        stage('Display Application URL') {
            steps {
                echo 'Application deployed successfully at http://localhost:8080'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully.'
        }
        failure {
            echo 'Pipeline execution failed.'
        }
    }
}