pipeline {
	agent { none }

	stages {
		stage('test') {
			steps {
				agent {
					docker {
						image 'node:alpine'
						args '-v /var/run/docker.sock:/var/run/docker.sock'
					}
				}
				echo 'Test node version'
				sh 'node --version'
			}
		}
	}
}
