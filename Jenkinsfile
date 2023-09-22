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
                    def pm2Output = sh(script: "pm2 start /var/www/html/pm2.json", returnStatus: true, returnStdout: true)
                    def pid = pm2Output.trim() // Trim any leading/trailing whitespace

                    // Print the PID to the console
                    echo "PM2 process started with PID: $pid"
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
