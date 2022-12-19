pipeline {
    agent any
    stages{
        stage('vcs'){
            steps{
                git branch: 'main'
                url: https://github.com/rohi3369/saleor.git
            }
        stage('docker image build'){
            steps{
                sh 'docker image build -t saleor:DEV'
            
            }
        }    
        }
    }
}