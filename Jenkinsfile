pipeline {
    agent any

	tools {
		maven 'M2_HOME'
	}

	// environment 
	// {
	//   MAVEN_HOME = "D:\Work\apache-maven-3.8.6\bin"
	//   JAVA_HOME = "D:\Work\jdk-17.0.5\bin"
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
