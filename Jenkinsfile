pipeline {
	agent {
		docker {
			image 'node:alpine'
		}
	}

	environment {
		DOCKER_HOST = 'tcp://192.168.1.22:4243'
	}

	stages {
		stage('test') {
			steps {
				echo 'Test node version'
				sh 'node --version'
			}
		}
	}
}
