pipeline {
    agent any
    stages {
        stage('Copy File to Destination') {
            steps {
                script {
                    sh "pm2 restart 0"
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
