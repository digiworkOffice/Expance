pipeline {
    agent any
        environment {
        localServerDir = '/var/www/html/expance'
    }
    stages {    
        stage('Pm2 start') {
            steps {
                script {
                    // Start or restart the PM2 process and capture the PID
                    //sh "pm2 reload /data/digimall/digimallimp/pm2.json"
                    sh "mkdir expance"
                    sh "cp -r * ${localServerDir}"
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
