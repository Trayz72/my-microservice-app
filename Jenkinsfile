@Library('my-lib') _

pipeline {
    agent any
    stages {
        stage('Greeting') {
            steps {
                script {
 
                    myCustomLog("Senior Dev", env.BRANCH_NAME)
                }
            }
        }
        stage('Code Checkout') {
            steps {
 
                checkout scm
            }
        }
	    stage('Testing Fail Scenario') {
            steps {
 
                eho "Running tests..."
            }
        }
    }

    
    post {
        always {
            script {
                    sendNotification(currentBuild.currentResult, "shahtanishq72@gmail.com")
            }
        }
    }
    
}
