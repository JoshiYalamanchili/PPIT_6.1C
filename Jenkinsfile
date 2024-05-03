pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Code is Being Built...'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Unit Tests are running...'
                echo 'Integration tests are running...'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Performing code analysis...'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'security scan is being performed...'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deployed into staging environment...'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Integration tests are being ran on staging environment...'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Being deploying into production environment...'
            }
        }
    }
 post {
        failure {
            // to send the email notifications if pipeline fails
            emailext attachLog: true,
                subject: "Pipeline Failure Notification",
                   body: "The Jenkins pipeline triggered a failure!",
                     to: 'joshithayalamanchili1@gmail.com'
        }
        success {
            // to send the email notifications if pipeline succeeds
            emailext attachLog: true,
                subject: "Pipeline Success Notification",
                   body: "The Jenkins pipeline triggered a success!",
                     to: 'joshithayalamanchili1@gmail.com'
        }
    }
}
