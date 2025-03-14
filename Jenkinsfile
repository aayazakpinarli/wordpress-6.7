pipeline {


    agent any





    environment {


        REMOTE_SSH_CREDENTIALS = 'd68edb7d-5537-4a51-b4f7-56f0f35c7d4f'


        REMOTE_HOST = 'aayaz'  


        REMOTE_DIR = '/var/deneme/' 


    }




    stages {

        stage('Checkout') {

            steps {


                script {


                    sh """


                        ssh -o StrictHostKeyChecking=no -i ${REMOTE_SSH_CREDENTIALS} user@${REMOTE_HOST} '


                            cd ${REMOTE_DIR} || mkdir -p ${REMOTE_DIR} && \


                            git pull origin main


                        '


                    """


                }

            }

        }
    }
}
