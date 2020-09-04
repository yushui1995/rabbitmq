pipeline {
	agent any
	options {
		buildDiscarder(logRotator(numToKeepStr: '5'))
                disableConcurrentBuilds()
		}
	stages {
		stage('build') {
		steps {
		echo "build stage"
		}
		post{
			always {
				echo "stage post alwasy"
			}
		}
	}
}	
	post {
		changed {
			echo "pipeline post changed"
		}
		always {
			echo "pipeline post alwasy"
		}
		success {
			echo "pipeline post success"
		}
	
	}
}
