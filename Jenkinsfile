pipeline {
    // master executor should be set to 0
    agent any
    stages {
	
	stage('Pull Latest Image') {
            steps {
                
                bat "docker pull shubhamit09/selenium-docker"
            }	
        }
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
		post
		{
		always
		{
			archiveArtifacts artifacts: '/*'
			 bat  "docker-compose down"
		}
		}
        
}