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
                post {
        success {
            mail to: "zara.danziger15@gmail.com",
                subject: "build status email",
                body: "test was successful!!"
        }
        failure {
          mail to: "zara.danziger15@gmail.com",
                subject: "build status email",
                body: "test failed!!"
        }
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
                post {
        success {
            mail to: "zara.danziger15@gmail.com",
                subject: "build status email",
                body: "security scan was successful!!"
        }
        failure {
          mail to: "zara.danziger15@gmail.com",
                subject: "build status email",
                body: "security scan failed!!"
        }
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
            mail to: "zara.danziger15@gmail.com",
                subject: "build status email",
                body: "build was successful!!"
        }
        failure {
          mail to: "zara.danziger15@gmail.com",
                subject: "build status email",
                body: "build was failed!!"
        }
    }
}
