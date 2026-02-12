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

	    stage('Testing Fail Scenario') {
            steps {
 
                echo "Running tests..."
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
