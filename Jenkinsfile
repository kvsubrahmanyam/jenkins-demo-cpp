pipeline {
	
	agent any

	stages {

		stage ('Clean') {
			steps {
				sh "git clean -fdx"
			}
		}

		stage('Build Server') {

			steps {
				sh "cd server && cmake . && make"
			}
		}

		stage('Build Client') {

			steps {
				sh "cd client && cmake . && make"
			}
		}
	}
}