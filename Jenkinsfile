pipeline {
    agent any

    environment {
        // Define environment variables for your GitHub and Docker Hub credentials
        GITHUB_USERNAME = credentials('zdrave123')
        GITHUB_PASSWORD = credentials('@Codexatlanticus1119')
        DOCKERHUB_USERNAME = credentials('zdrave123')
        DOCKERHUB_PASSWORD = credentials('@Codexatlanticus1119')
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout your repository from GitHub
                git credentialsId: 'zdrave123', url: 'https://github.com/zdrave123/my-pipeline-repo.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                // Build and tag the Docker image
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'zdrave123') {
                        def dockerImage = docker.build('zdrave123/projectOne')
                        dockerImage.push()
                    }
                }
            }
        }
        stage('Test') {
            steps {
                // Add your test commands here
            }
        }
        stage('Deploy') {
            steps {
                // Add your deployment commands here
            }
        }
    }
}
