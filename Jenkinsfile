pipeline {
    agent any

    stages {
        stage('1-Build') {
            steps {
                git branch: 'main', url: 'https://github.com/aamerinov20/simple_nodejs.git'
            }
        }
        stage('2-Test') {
            steps {
                mkdir(dir:"testfolder123333")
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