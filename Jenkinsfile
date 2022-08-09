pipeline {
    agent any

    environment {
        DOCKERHUB_CREDENTIALS = credentials('dockerhub_cred')
        REGISTRYHUB           = 'aamerinov20/web_alisher'
    }

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/aamerinov20/simple_nodejs.git'
            }
        }
        stage('Build Image') {
            steps {
                sh 'docker build . -t $REGISTRYHUB'
            }
        }
        stage('Deploy container') {
            steps {
                sh 'docker-compose up -d'
            }
        }
        stage('Upload to DockerHub') {
            steps {
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
                sh 'docker push $REGISTRYHUB'
                sh 'docker logout'

            }
        }
    }
}