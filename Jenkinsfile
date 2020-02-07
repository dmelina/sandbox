import groovy.json.JsonSlurperClassic

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

        def payload = '{ "name": "John Doe" } /* some comment */'

        def result = toJson(payload)

        sh "echo ${result}"
        
        //assert object instanceof Map
        //assert object.name == 'John Doe'

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

@NonCPS
def toJson(String object) {
  def jsonSlurper = new JsonSlurperClassic()
  return jsonSlurper.parseText(object)
  //assert parse instanceof Map
}
