pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the GitHub repository
                git 'https://github.com/naeemamaze/webapplicationguvi.git'
            }
        }

        stage('Build') {
            steps {
                // If you have a build process (e.g., npm, yarn, etc.), add the build commands here.
                // For static HTML files, you can leave this stage empty.
            }
        }

        stage('Docker Build and Push') {
            steps {
                // Build the Docker image and push to Docker Hub
                def dockerImage = docker.build("naeemamaze/webserver:latest")
                dockerImage.push()
            }
        }
    }
}
