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
                    emailext attachLog: true,
                        to: "zara.danziger15@gmail.com",
                        subject: "Build Status: Success",
                        body: "Unit and integration tests were successful!"
                }
                failure {
                    emailext attachLog: true,
                        to: "zara.danziger15@gmail.com",
                        subject: "Build Status: Failure",
                        body: "Unit and integration tests failed!"
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
                    emailext attachLog: true,
                        to: "zara.danziger15@gmail.com",
                        subject: "Security Scan Status: Success",
                        body: "Security scan was successful!"
                }
                failure {
                    emailext attachLog: true,
                        to: "zara.danziger15@gmail.com",
                        subject: "Security Scan Status: Failure",
                        body: "Security scan failed!"
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



