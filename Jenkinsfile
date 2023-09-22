pipeline {
    agent any
    environment {
        localServerDir = '/var/www/html/server'
    }
    stages {  
     stage('Pm2 start') {
            steps {
                script {
                    // Copy the file to the destination folder
                    // sh "pm2 start /var/www/html/pm2.json"
                    sh "pm2 ls"
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
