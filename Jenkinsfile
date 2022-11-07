pipeline {
    agent any

	tools {
		maven 'M2_HOME'
	}

	// environment {
	// 	MAVEN_HOME = "E:\destro\Maven\apache-maven-3.6.3\bin"
	// }

    stages {
		stage('Clone-Repo') {
			steps {
				checkout scm
			}
		}
	
		stage('Build') {
			steps {
				 'mvn install -Dmaven.test.skip=true'
			}
		}
		
		stage('Unit Tests') {
			steps {
				 'mvn compiler:testCompile'
				 'mvn surefire:test'
			}
		}

	
		stage('Deployment') {
			steps {
				echo "hellow_world"
				
	    	}
		}
    }
}
