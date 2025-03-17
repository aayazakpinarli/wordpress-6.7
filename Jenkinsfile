pipeline {
    agent any
    environment {
        TARGET_VM = "aayaz@35.242.207.186"
        REPO_URL = "https://github.com/aayazakpinarli/wordpress-6.7.git"
        DEST_DIR = "home/aayaz/deneme"
    }
    stages {
        stage('Clone Repository on Remote VM') {
            steps {
                script {
                    sshagent(['app-vm']) { 
                        sh """
                        ssh -o StrictHostKeyChecking=no \$TARGET_VM '
                        if [ ! -d "\$DEST_DIR/.git" ]; then
                            git clone \$REPO_URL \$DEST_DIR
                        else
                            cd \$DEST_DIR && git pull origin main
                        fi'
                        """
                    }
                }
            }
        }
    }
}
