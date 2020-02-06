pipeline {

	agent none

	stages {
		stage('test-node') {
			agent {
				docker {
					image 'node:alpine'
					args '-v /var/run/docker.sock:/var/run/docker.sock'
				}
			}
			steps {
				echo 'Test node version'
				sh 'ls -l'
				sh 'node --version'
			}
		}
		stage('test-golang') {
			agent {
				docker {
					image 'golang:alpine'
					args '-v /var/run/docker.sock:/var/run/docker.sock'
				}
			}
			steps {
				echo 'Test go version'
				sh 'ls -l'
				sh 'go version'
			}
		}
	}
}
