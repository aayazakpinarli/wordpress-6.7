pipeline {
    agent any
    stages {
        stage('Connect to VM') {
            steps {
                sshagent(['app-connection']) {
                        sh '''
                        ssh -o StrictHostKeyChecking=no aayaz@35.242.207.186 << 'EOF'
                        echo "Connected to VM!"
                        sudo apt update -y
                        sudo apt install git -y
                        cd /var/www/
                        git clone https://github.com/aayazakpinarli/wordpress-6.7
                        echo "Repository cloned successfully!"
                        EOF
                    '''
                }
            }
        }
    }
}
