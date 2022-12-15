pipeline {
	//agent any
	//agent { docker { image 'maven:3.6.3'}}
	agent { docker { image 'node:18.12.1'}}
	stages {
		stage("Build") {
			steps{
				echo "Build"
			}

		}
		stage("Test") {
			steps{
				sh "node --version"
	            echo "Test"
			}

		}
		stage("Integration Test") {
			steps{
	            echo "Integration Test"
			}

		}
	}

	post {
		always{
			echo "I am running always."
		}
		success{
			echo "I am running when you are successful."
		}
		failure{
			echo "I am running when you are failure."
		}
	} 
}
