pipeline {
    // master executor should be set to 0
    agent any
    stages {
        stage('Start Grid') {
            steps {
                
                bat "docker-compose up -d hub chrome"
            }	
        }
		
		
		stage('Running the test') {
            steps {
                
                bat "docker-compose up testng1"
            }	
        }
		
		}
		Post
		{
		always
		{
			archiveArtifacts artifacts: 'output/**'
			 bat  "docker-compose down"
		}
		}
        
}