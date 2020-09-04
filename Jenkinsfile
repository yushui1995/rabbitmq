pipeline {
	agent any
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
	options {
		buildDiscarder(logRotator(numTokeeStr: '5'))
		}	
	}
}
