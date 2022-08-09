pipeline {
    agent any

    stages {
        stage('1-Build') {
            steps {
                git clone branch: 'main', url: 'https://github.com/aamerinov20/simple_nodejs.git'
            }
        }
        stage('2-Test') {
            steps {
                sh 'mkdir testfolderr122222'
            }
        }
        stage('3-Deploy') {
            steps {
                echo "Start of Stage Deploy"
                echo "Deploying......."
                echo "End of Stage Build"
            }
        }
    }
}