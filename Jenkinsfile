pipeline {
    agent any
    
    stages {
        stage('Build and Publish') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
