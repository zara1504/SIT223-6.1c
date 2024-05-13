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
                             subject: "Unit and Integration Test Status",
                             body: "Unit and integration tests were successful!"
                }
                failure {
                    emailext attachLog: true,
                             to: "zara.danziger15@gmail.com",
                             subject: "Unit and Integration Test Status",
                             body: "Unit or integration tests failed!"
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
                             subject: "Security Scan Status",
                             body: "Security scan was successful!"
                }
                failure {
                    emailext attachLog: true,
                             to: "zara.danziger15@gmail.com",
                             subject: "Security Scan Status",
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
    post {
        always {
            cleanWs()
        }
    }
}


