pipeline {
    agent any  // Use any available Jenkins agent

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub repository
                git 'https://github.com/codingAjayKumar/mock-company-webapp.git'
            }
        }
        
        stage('Build') {
            steps {
                // Run Gradle build to assemble the application
                sh './gradlew assemble'
            }
        }
        
        stage('Test') {
            steps {
                // Run Gradle test to execute tests
                sh './gradlew test'
            }
        }
    }

    post {
        success {
            echo 'Build and tests completed successfully.'
        }
        failure {
            echo 'Build or tests failed.'
        }
    }
}
