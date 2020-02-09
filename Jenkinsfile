import groovy.json.JsonSlurperClassic

pipeline {

//	agent any
	agent {
		docker {
			image 'golang:alpine'
		}
	}

	stages {
		stage('test-golang') {
			steps {
        script {
				sh 'printenv'
				sh 'go version'
        }
			}
		}
		stage('json-parse') {
			steps {
        script {

        def payload = '{ "name": "John Doe" } /* some comment */'
        def result = parseJson(payload)
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
def parseJson(String object) {
  def jsonSlurper = new JsonSlurperClassic()
	def toto = jsonSlurper.parseText(object)
	def tata = "test"
	return tata
  //assert parse instanceof Map
}
