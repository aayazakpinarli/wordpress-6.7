pipeline {
    agent any
    stages {
        stage('Connect to VM') {
            steps {
                sshagent(['app-connection']) {
                        sh '''
                        ssh -o StrictHostKeyChecking=no aayaz@35.242.207.186 "
                        echo 'Connected to VM!';
                        cd /var/www/;
                        sudo git clone https://github.com/aayazakpinarli/wordpress-6.7;
                        sudo git clone https://github.com/aayazakpinarli/wordpress-6.6;
                        sudo git clone https://github.com/aayazakpinarli/wordpress-6.5;
                        echo 'Repositories are cloned successfully!';
                        "
                    '''
                }
            }
        }
    }
}
