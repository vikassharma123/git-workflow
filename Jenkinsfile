pipeline {
	agent any

	stages {
	   stage('Build') {
   		steps {
			docker build . -t webapp:latest
		      }
		}
	
	
		stage('Deploy') {
		steps {
			docker run -p 81:80 -d webapp:latest
			  }
		
		}
	}
}
