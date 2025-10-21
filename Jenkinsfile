pipeline {
    agent any
    stages {
        stage('Git checkout') {
            steps {
                sh 'echo "Checkout git based project"'
                git branch: 'main', credentialsId: 'jenkins_cred', url: 'https://github.com/Chukwumaeke/docker_local.git'
            }
        }

    }
}

