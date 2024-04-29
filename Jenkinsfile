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
            mail to: "zara.danziger15@gmail.com",
                subject: "build status email",
                body: "unit integration test was successful!!"
        }
        failure {
          mail to: "zara.danziger15@gmail.com",
                subject: "build status email",
                body: "unit integration test failed!!"
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
