pipeline {
    agent any
    stages {
        stage('Init') {
            steps {
                bat 'terraform init'
            }
        }
        stage('Plan') {
            steps {
                bat 'terraform plan'
            }
        }
        stage('Apply') {
            steps {
                input 'Apply the changes?'
                bat 'terraform apply -auto-approve'
            }
        }
    }
}
