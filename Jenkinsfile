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
				sh "cd server"
				sh "cmake ."
				sh "make"
			}
		}

		stage('Build Client') {

			steps {
				sh "cd client"
				sh "cmake ."
				sh "make"
			}
		}
	}
}