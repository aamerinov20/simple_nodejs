pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/aamerinov20/simple_nodejs.git'
            }
        }
        stage('Build Image') {
            steps {
                sh 'docker build . -t web_alisher'
            }
        }
        stage('Deploy container') {
            steps {
                

            }
        }
    }
}