pipeline {

//	agent none
		agent {
			docker {
				image 'node:alpine'
			}
		}

	environment {
		DOCKER_HOST = 'tcp://192.168.1.22:4243'
	}

	stages {
		stage('test-node') {
			steps {
				echo 'Test node version'
				sh 'ls -l'
				sh 'node --version'
			}
		}
		//stage('test-golang') {
		//	agent {
		//		docker {
		//			image 'golang:alpine'
		//		}
		//	}
		//	steps {
		//		echo 'Test go version'
		//		sh 'ls -l'
		//		sh 'go version'
		//	}
		//}
	}
}
