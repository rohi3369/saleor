pipeline {
    agent any
    stages{
        stage('vcs'){
            steps{
                git branch: 'main',
                url: 'https://github.com/rohi3369/saleor.git'
            }
        }
        stage('docker image build'){
            steps{
                sh """
                sudo chown ubuntu:docker /var/run/docker.sock
                docker image build -t sale:dev .
                docker image tag sale:dev sai3369/sale:dev
                docker push sai3369/sale:dev
                """
            }
        }    
    }
}
