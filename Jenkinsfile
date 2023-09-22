pipeline {
    agent any
       environment {
        localServerDir = '/home/digitech/server_new/server'
    }
    stages {    
        stage('Pm2 start') {
            steps {
                script {
                    // Start or restart the PM2 process and capture the PID
                   sh "pm2 start /home/digitech/server_new/server/pm2.json"

                }
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}
