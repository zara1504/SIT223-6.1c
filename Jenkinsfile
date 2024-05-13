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
                    sendEmail(email: "zara.danziger15@gmail.com", subject: "Build Status: Unit and Integration Tests - Success", body: "Unit and Integration Tests were successful!")
                }
                failure {
                    sendEmail(email: "zara.danziger15@gmail.com", subject: "Build Status: Unit and Integration Tests - Failed", body: "Unit and Integration Tests failed!")
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
                    sendEmail(email: "zara.danziger15@gmail.com", subject: "Build Status: Security Scan - Success", body: "Security scan was successful!")
                }
                failure {
                    sendEmail(email: "zara.danziger15@gmail.com", subject: "Build Status: Security Scan - Failed", body: "Security scan failed!")
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

def sendEmail(email, subject, body) {
    emailext (
        to: email,
        subject: subject,
        body: body,
        attachmentsPattern: '**/*.log'
    )
}

