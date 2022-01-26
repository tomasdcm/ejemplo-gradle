pipeline {
    agent any

    environment {
	    STAGE = ''
	}
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Building..'
            }
        post {
            always {
                	slackSend color: 'good', message: '[tomasdcm][taller-slack][maven] Ejecucion exitosa'
                }
            }
           
        }
    }
}
