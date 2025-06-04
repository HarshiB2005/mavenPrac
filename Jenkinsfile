pipeline {
	agent any
	
	tools {
		maven 'Maven'
	}
	
	stages {
		stage('Checkout') {
			steps {
				git branch: 'master', url:'https://github.com/HarshiB2005/mavenPrac.git'
			}
		}
		
		stage('Build') {
			steps {
				sh 'mvn clean package'
			}
		}
		
		stage('Test') {
			steps {
				sh 'mvn test'
			}
		}
		
		stage('Run Application') {
			steps {
				sh 'java -jar target/maven-1.0-SNAPSHOT.jar'
			}
		}
	}
}
