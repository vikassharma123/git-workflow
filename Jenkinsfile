pipeline {
	agent any

	stages {
	   stage('Build') {
   		steps {
			docker build . -t master-website:latest
		      }
		}
	
	
		stage('Deploy') {
		steps {
			docker stop master-website:latest
			docker rm master-website:latest
			docker run -p 81:80 -d master-website:latest
			  }
		
		}
	}
}
