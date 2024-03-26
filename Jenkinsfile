pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/sagari-a/terraform_cicd_jenkins.git'
            }
         stage('init') {
            steps {
                sh "terraform init"
            }
        }
        stage('plan') {
            steps {
                sh "terraform plan"
            }
        }
        stage('action') {
            steps {
                sh "terraform ${action} -auto-approve"
            }
        }
    }
}
