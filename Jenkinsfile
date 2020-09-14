pipeline {
    agent any

	environment {
		ENVIRONMENT = "PROD"
	}
	
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the main repository'
				checkout([$class: 'GitSCM', 
						  branches: [[name: '${GIT_BRANCH}']],
					 userRemoteConfigs: [[url: 'https://github.com/Chi996/jenkins-test-project3.git']]])
            }
        }
        stage('Finished') {
            steps {
                echo 'finished'
            }
        }
    }
}