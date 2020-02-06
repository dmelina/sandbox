pipeline {

	agent none

	stages {
		stage('test') {
			agent {
				docker {
					image 'node:alpine'
					args '-v /var/run/docker.sock:/var/run/docker.sock'
				}
			}
			steps {
				echo 'Test node version'
				sh 'node --version'
			}
		}
	}
}
