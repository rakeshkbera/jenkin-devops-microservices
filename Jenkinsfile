pipeline {
	agent any
	stages {
		stage("Build") {
			steps{
				echo "Build"
			}

		}
		stage("Test") {
			steps{
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
