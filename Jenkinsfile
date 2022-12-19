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
                sh 'docker image build -t saleor:0.2 .'
            }
        }
        
    }
}    