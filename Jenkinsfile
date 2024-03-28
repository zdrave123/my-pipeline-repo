pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the Docker image...'
                sh 'docker build -t my-docker-image .'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deployment commands here
            }
        }
    }
}
