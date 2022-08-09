pipeline {
    agent any

    stages {
        stage('1-Build') {
            steps {
                git url: 'https://github.com/aamerinov20/simple_nodejs.git'
            }
        }
        stage('2-Test') {
            steps {
                echo "Start of Stage Test"
                echo "Testing......."
                echo "End of Stage Build"
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