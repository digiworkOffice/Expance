pipeline {
    agent any
    environment {
        localServerDir = '/var/www/html/server'
    }
    stages {  
        stage('Pm2 start') {
            steps {
                script {
                    // Start or restart the PM2 process and capture the PID
                   // def pm2Output = sh(script: "pm2 start /home/digitech/pm2.json")

                    // Save the PID to a file for future reference (optional)

                    sh "pm2 kill"

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
