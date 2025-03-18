pipeline {
    agent any
    stages {
        stage('Connect to VM') {
            steps {
                sshagent(['app-connection']) {
                    sh 'ssh -o StrictHostKeyChecking=no aayaz@35.242.207.186 "echo Connected to VM!"'
                }
            }
        }
    }
}
