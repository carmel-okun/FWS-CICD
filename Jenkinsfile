pipeline {
    agent any

    stages {
        stage('Cloning Git') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/carmel-okun/FWS-CICD.git']]])
            }
        }
        stage('update app') {
            steps {
                sh "pwd"
                sh "cd /var/lib/jenkins/workspace/CICD-FWS/src/"
                sh "docker-compose up -d"
            }
        }
    }
}

