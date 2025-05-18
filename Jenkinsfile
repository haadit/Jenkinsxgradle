pipeline {
    agent any
    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                // Replace Maven build command with Gradle
                bat './gradlew clean build'  // Assuming you have the Gradle wrapper
            }
        }
        stage('Test') {
            steps {
                // Add testing step if needed
                bat './gradlew test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
