pipeline {
    agent any

    stages {
        stage('pull code') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '9d792add-1bc1-4f91-aa7f-b999bfea9fa7', url: 'git@github.com:xiaojin111/gitTest.git']]])
            }
        }
        stage('build project') {
            steps {
                sh label: '', script: '''source /etc/profile
                go build sss.go'''
            }
        }
        stage('publish project') {
            steps {
                echo 'publish project'
            }
        }
    }
}