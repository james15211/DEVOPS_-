pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Grabs the latest code from GitHub
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Add your build commands here (e.g., sh 'npm install' or sh 'make')
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here (e.g., sh 'npm test' or sh 'pytest')
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to staging/production...'
                // Add deployment commands here (e.g., Docker run, Kubernetes apply, or SCP)
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the logs.'
        }
    }
}
