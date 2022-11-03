pipeline {
    agent any

	tools {
		maven 'MAVEN_HOME'
	}

	environment {
		MAVEN_HOME = "E:\destro\apache-maven-3.8.6\bin"
	}

    stages {
		stage('Clone-Repo') {
			steps {
				checkout scm
			}
		}
	
		stage('Build') {
			steps {
				sh 'mvn install -Dmaven.test.skip=true'
			}
		}
		
		stage('Unit Tests') {
			steps {
				sh 'mvn compiler:testCompile'
				sh 'mvn surefire:test'
			}
		}

	
		// stage('Deployment') {
		// 	steps {
		// 		sh 'sshpass -p "admin" scp target/gamutgurus.war admin@172.17.0.4:/home/admin/'
				
	    	}
		}
    }
}
