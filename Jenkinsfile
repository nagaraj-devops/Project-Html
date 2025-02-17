pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/nagaraj-devops/Project-Html.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t my-html-app .'
                }
            }
        }
        stage('Run Container') {
            steps {
                script {
                    sh 'docker run -d -p 8080:80 my-html-app'
                }
            }
        }
    }
}
