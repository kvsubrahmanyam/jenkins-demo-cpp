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
				sh "cd server && cmake -G 'Visual Studio 16 2019'"
			}
		}

		stage('Build Client') {

			steps {
				sh "cd client && cmake -G 'Visual Studio 16 2019'"
			}
		}
	}
}
