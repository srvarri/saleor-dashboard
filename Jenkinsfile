pipeline {
    agent any
    stages {
        stage('vcs') {
            steps {
                git branch: 'main', url: 'https://github.com/WorkshopsByKhaja/saleor-dashboard.git'
            }
        }
        stage('docker image build') {
            steps {
                sh 'docker image build -t srvarri/saleor-dashboar:dv .'
            }
        }
        stage('push image to registry') {
            steps {
                sh 'docker image push srvarri/saleor-dashboar:Dv'
            }
        }
    }
}    