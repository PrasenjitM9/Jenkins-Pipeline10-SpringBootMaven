pipeline {
	agent any
	
	tools {
		jdk "Java_Home"
		maven "Maven_Home"
	}
	stages {
	   stage ('Compile Stage') {

		steps {
		   
  		   withMaven(maven : 'Maven_Home') {
			bat 'mvn clean compile'
		    }
		}
	    }

	    stage ('Testing stage') {
		
		steps {

		   withMaven(maven : 'Maven_Home') {
			bat 'mvn test'
		   }
		}
	     }

	     stage ('Packaging Stage') {

		steps {

		   withMaven(maven : 'Maven_Home') {
			bat 'mvn package'
		   }
		}
	      }
	   }
}
