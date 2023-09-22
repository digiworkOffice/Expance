pipeline {
    agent any
    environment {
        localServerDir = '/var/www/html/server'
    }
    stages {
stage('install npm') {
            steps {                
                    sh "npm i -f"
            }
}
       
        stage('Deploy to Local Server') {
            steps {  
                sh "rm -rf ${localServerDir}/*"
   
                sh "cp -r * ${localServerDir}"

                 echo "content copied to ${localServerDir}"
            }
        }
     stage('Pm2 start') {
            steps {
                script {
                    // Copy the file to the destination folder
                    sh "pm2 start /var/www/html/pm2.json"
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
