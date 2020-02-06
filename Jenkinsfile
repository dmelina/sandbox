pipeline {

//	agent none
	agent {
		docker {
			image 'node:alpine'
		}
	}

	stages {
		stage('test-node') {
			steps {
				echo 'Test node version'
				sh 'ls -l'
				sh 'printenv'
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
