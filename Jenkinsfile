pipeline {
    agent any

    stages {
        stage('git-clone') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'e16a40dd-3877-40a9-949a-585730e7833b', url: 'https://github.com/Karan8808/terraform-php.git']])
            }
        }
        stage('tf-init') {
            steps {
                sh 'terraform init'
            }
        }
        stage('tf-init') {
            steps {
                sh 'terraform apply -auto-approve'
            }
        }
    }
}
