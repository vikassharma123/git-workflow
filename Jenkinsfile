pipeline {
	agent any

	stages {
	   stage('Build') {
   		steps {
			sh 'docker build . -t master-website:latest'
		      }
		}
	
	
		stage('Deploy') {
		steps {
			sh 'docker run -p 81:80 -d master-website:latest'
			  }
		
		}
	}
}
