//node {
//	stage('Build') {
//		echo "Build"
//	}
//	stage('Test') {
//		echo "Test"
//	}
//}
//Declarative pipeline
pipeline {
	//agent any
	agent { docker { image 'maven:3.6.3' } }
	stages {
		stage('Build'){
			steps{
				echo 'mvn --version'
				echo "Build"
			}
		}
		stage('Test'){
			steps{
				echo "Test"
			}
		}
		stage('Integration'){
			steps{
				echo "Integration"
			}
		}
	} 
	
	post {
		always {
			echo "I am awesome. I will always run"
		}
		success {
			echo "I am successful"
		}
		failure {
			echo "I am failed"
		}
	}
}
