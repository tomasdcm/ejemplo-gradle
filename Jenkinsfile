pipeline {
    agent any

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
                // slackSend "Build deployed successfully"
                echo 'Building..'
            }
        post {
            always {
                slackSend color: 'good', message: '[tomasdcm][taller-slack][maven] Ejecuci&#243;n exitosa'
                }
            }
           
        }
    }
}
