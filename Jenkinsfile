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
                   sh "cd /var/www/html/server && pm2 start ./server.js"

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
