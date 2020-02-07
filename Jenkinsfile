import groovy.json.JsonSlurper

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
				sh 'printenv'
				sh 'node --version'
        }
			}
		}
		stage('json-parse') {
			steps {
        script {

        def jsonSlurper = new JsonSlurper()
        def object = jsonSlurper.parseText('{ "name": "John Doe" } /* some comment */')
        
        assert object instanceof Map
        assert object.name == 'John Doe'

        sh "echo ${object.name}"
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
