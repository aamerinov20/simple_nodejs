pipeline{

	agent { docker 'ubuntu:latest' }

	environment {
		DOCKERHUB_CREDENTIALS=credentials('dockerHub')
	}

	stages {
	    
	    stage('gitclone') {

			steps {
				git 'https://github.com/aamerinov20/simple_nodejs.git'
			}
		}

		stage('Build') {

			steps {
				sh 'docker build -t web_alisher:latest .'
			}
		}

		stage('Login') {

			steps {
				sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
			}
		}

		stage('Push') {

			steps {
				sh 'docker push web_alisher:latest'
			}
		}
	}


}