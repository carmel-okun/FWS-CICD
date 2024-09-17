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
                sh "cd ./src/"
                sh "docker-compose up -d"
            }
        }
    }
}

