pipeline {
    agent any
    tools {
        maven 'maven3.9'
    }
    stages {
        stage('Git checkout') {
            steps {
                sh 'echo "Checkout git based project"'
                git branch: 'main', credentialsId: 'jenkins_cred', url: 'https://github.com/Chukwumaeke/docker_local.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
       }
       stage ('Archive artifacts') {
            steps {
                archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
            }
        } 
    }
}
