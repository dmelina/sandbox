pipeline {

//	agent any
	agent {
		docker {
			image 'node'
		}
	}

	stages {
		stage('test-node') {
			steps {
        script {
				echo 'Test node version'
				sh 'ls -l'
				sh 'printenv'
				sh 'node --version'

        def jsonObj = readJSON text: jsonString

        assert jsonObj['name'] == 'katone'  // this is a comparison.  It returns true
        sh "echo ${jsonObj.name}"  // prints out katone
        sh "echo ${jsonObj.age}"   // prints out 5
        }
			}
		}
		stage('json-parse') {
			steps {
        script {
        def jsonObj = readJSON text: jsonString
        assert jsonObj['name'] == 'katone'  // this is a comparison.  It returns true
        sh "echo ${jsonObj.name}"  // prints out katone
        sh "echo ${jsonObj.age}"   // prints out 5
        }
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
