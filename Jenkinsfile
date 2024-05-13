pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the code...'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests...'
                echo 'Running integration tests...'
            }
            post {
                success {
                    emailext body: "Unit integration test was successful!", 
                             subject: "Build Status: Success", 
                             to: "zara.danziger15@gmail.com", 
                             attachmentsPattern: '**/*.log'
                }
                failure {
                    emailext body: "Unit integration test failed!", 
                             subject: "Build Status: Failure", 
                             to: "zara.danziger15@gmail.com", 
                             attachmentsPattern: '**/*.log'
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Performing code analysis...'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scan...'
            }
            post {
                success {
                    emailext body: "Security scan was successful!", 
                             subject: "Security Scan Status: Success", 
                             to: "zara.danziger15@gmail.com", 
                             attachmentsPattern: '**/*.log'
                }
                failure {
                    emailext body: "Security scan failed!", 
                             subject: "Security Scan Status: Failure", 
                             to: "zara.danziger15@gmail.com", 
                             attachmentsPattern: '**/*.log'
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging server...'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production server...'
            }
        }
    }
}






