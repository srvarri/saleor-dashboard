pipeline {
    agent any
    stages {
        stage('vcs') {
            steps {
                git branch: 'main', url: 'https://github.com/srvarri/saleor-dashboard.git'
            }
        }
        stage('image build') {
            steps {
                sh 'docker image build -t srvarri/saleor:v.1 .'
            }
        }
        stage('push image') {
            steps {
                sh 'docker image push srvarri/saleor:v.1'
            }
        }
        
    }
}    
