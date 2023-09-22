pipeline {
    agent any
    stages {    
        stage('Pm2 start') {
            steps {
                script {
                    // Start or restart the PM2 process and capture the PID
                    sh "pm2 reload /data/digimall/digimallimp/pm2.json"
                    //sh "pm2 ls"

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
