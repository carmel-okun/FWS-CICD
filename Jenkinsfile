pipeline {
    agent any

    stages {
        stage('Cloning Git') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/carmel-okun/FWS-CICD.git']]])
            }
        }
        stage('run main.py') {
            steps {
                withAWS(credentials: 'AWS Credentials', region: 'us-east-1') {
                    echo pwd
                    sh "cd ./src/"
                    sh "docker-compose up -d"
                }
            }
        }
    }
}

