pipeline {
    agent any

    environment {
        // Define the global environment variables
        MAVEN_HOME = '/usr/local/maven'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application using Maven'
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests'
                echo 'Running integration tests'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Analyzing the code with SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing security scan with OWASP ZAP'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to AWS EC2 Staging Environment'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging environment'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to AWS EC2 Production Environment'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}