pipeline {
    agent any
    stages {
        stage('Copy File to Destination') {
            steps {
                script {
                    sh "pm2 reload /var/www/html/pm2.json"
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
