pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build("simple-python-devops")
                }
            }
        }
        stage('Test') {
            steps {
                // Add steps to run tests
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                script {
                    dockerImage.run("-p 4000:80")
                }
            }
        }
    }
}
