pipeline {
	agent {
		docker {
			image 'node:alpine'
			args '-v /var/run/docker.sock:/var/run/docker.sock'
		}
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
