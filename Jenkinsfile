pipeline {
    agent any

    environment {
        REMOTE_SSH_CREDENTIALS = 'd68edb7d-5537-4a51-b4f7-56f0f35c7d4f'
        REMOTE_HOST = '35.242.207.186'  
        REMOTE_DIR = '/var/' 
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    sh """
                        ssh aayaz@${REMOTE_HOST} '
                            git pull origin main
                        '
                    """
                }
            }
        }
    }
}
