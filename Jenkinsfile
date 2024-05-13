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
                always {
                    emailext(
                        to: "zara.danziger15@gmail.com",
                        subject: "Jenkins Build:${currentBuild.fullDisplayName}",
                        body: "<p>Stage 'Unit and Integration Tests' completed with status ${currentBuild.result}</p> <p>Check console output at ${env.BUILD_URL} to view the result.</p>",
                        attachLog: true
                    )
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
                always {
                    emailext(
                        to: "zara.danziger15@gmail.com",
                        subject: "Jenkins Build:${currentBuild.fullDisplayName}",
                        body: "<p>Stage 'Security Scan' completed with status ${currentBuild.result}</p><p>Check console output at ${env.BUILD_URL} to view the result.</p>",
                        attachLog: true
                    )
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








