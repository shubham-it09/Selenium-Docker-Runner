pipeline {
    // master executor should be set to 0
    agent any
    stages {
        stage('Run Test') {
            steps {
                
                bat "docker-compose up"
            }	
        }
		
		
        stage('Build Grid Down') {
            steps {
                //sh
                bat  "docker-compose down"
            }
        }
		
		}
        
}