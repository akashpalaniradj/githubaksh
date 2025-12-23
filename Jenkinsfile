pipeline {
    agent any

    environment {
        IMAGE_NAME = "akashpalaniradj/flask-ci-cd"
        IMAGE_TAG  = "latest"
    }

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/akashpalaniradj/githubaksh.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat "docker build -t %IMAGE_NAME%:%IMAGE_TAG% ."
            }
        }

        stage('Push Docker Image') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'dockerhub-creds',
                    usernameVariable: 'DOCKER_USER',
                    passwordVariable: 'DOCKER_PASS'
                )]) {
                    bat '''
                    echo %DOCKER_PASS% | docker login -u %DOCKER_USER% --password-stdin
                    docker push %IMAGE_NAME%:%IMAGE_TAG%
                    '''
                }
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                bat "kubectl apply -f deployment.yaml"
            }
        }
    }
}
