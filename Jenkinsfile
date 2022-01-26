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
                echo 'Deploying..'
            }
        post {
            	success {
                	slackSend color: 'good', message: '[tomasdcm][taller-slack][maven] Ejecucion exitosa'
                }
		failure {
		   	slackSend color: 'danger', message: '[tomasdcm][taller-slack][maven] Ejecucion fallida en stage ${STAGE}'
                }
            }
           
        }
    }
}
