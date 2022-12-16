pipeline {
	agent any
	//agent { docker { image 'maven:3.6.3'}}
	//agent { docker { image 'node:18.12.1'}}
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage("Build") {
			steps{
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
				echo "$PATH"
				echo "BUILD_NUMBER -$env.BUILD_NUMBER"
				echo "BUILD ID - $env.BUILD_ID"
				echo "BUILD TAG - $BUILD_TAG"
				echo "JON NAME - $JOB_NAME"
				echo " BUILD URL - $BUILD_URL"
			}

		}
		stage("Test") {
			steps{
				//sh "node --version"
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
