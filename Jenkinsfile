pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Unit Tests') {
            steps { 
                echo 'Unit testing...'
            }
        }
        stage('Integration Tests') {
            steps {
                echo 'Integration testing...'
            }
        }
        stage('Check Lint') {
            steps {
                echo 'Lint...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
    post {
        always {
            slackSend "Build Finished - ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)" 
        }
    }
}