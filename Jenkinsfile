pipeline {
	agent any
	
	tools {
		jdk "Java_Home"
		maven "Maven_Home"
	}
	stages {
	   stage ('Compile Stage') {
		steps {
			bat 'mvn clean compile'
		    }
		}

	    stage ('Testing stage') {
		
		steps {
			bat 'mvn test'
		   }
		}
	     stage ('Packaging Stage') {
		steps {
			bat 'mvn package'
		   }
		}
	   }
	}
