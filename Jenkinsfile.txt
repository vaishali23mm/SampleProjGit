pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Example build step
                bat 'echo Building...'
            }
        }
        stage('Test') {
            steps {
                // Example test step
                bat 'echo Testing...'
            }
        }
        stage('Deploy') {
            steps {
                // Example deploy step
                bat 'echo Deploying...'
            }
        }
    }
    
    post {
        success {
            // Actions to be performed if pipeline succeeds
            echo 'Pipeline succeeded! Sending notification...'
        }
        failure {
            // Actions to be performed if pipeline fails
            echo 'Pipeline failed! Sending notification...'
        }
        always {
            // Actions to be performed always, regardless of pipeline result
            echo 'Cleaning up...'
        }
    }
}
