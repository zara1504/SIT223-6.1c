pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Placeholder step for building the code
                echo 'Building the code...'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                // Placeholder step for running unit tests
                echo 'Running unit tests...'
                // Placeholder step for running integration tests
                echo 'Running integration tests...'
            }
        }
        stage('Code Analysis') {
            steps {
                // Placeholder step for code analysis
                echo 'Performing code analysis...'
            }
        }
        stage('Security Scan') {
            steps {
                // Placeholder step for security scan
                echo 'Performing security scan...'
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Placeholder step for deploying to staging
                echo 'Deploying to staging server...'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                // Placeholder step for running integration tests on staging
                echo 'Running integration tests on staging...'
            }
        }
        stage('Deploy to Production') {
            steps {
                // Placeholder step for deploying to production
                echo 'Deploying to production server...'
            }
        }
    }
    
    post {
        success {
            emailext (
                subject: "Pipeline Success: ${currentBuild.fullDisplayName}",
                body: "The pipeline completed successfully. No further action required.",
                to: "zara.danziger15@gmail.com",
                attachLog: true
            )
        }
        failure {
            emailext (
                subject: "Pipeline Failure: ${currentBuild.fullDisplayName}",
                body: "The pipeline failed. Please check the Jenkins console output for more details.",
                to: "zara.danziger15@gmail.com",
                attachLog: true
            )
        }
    }
}
