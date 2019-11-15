
pipeline {
    agent any

    stages {
        
        stage('build') {
            steps {
                bat label: '', script: 'mvn install '
            }
        }
        
        
        stage('checkout') {
            steps {
                git 'https://github.com/MradhoussemGeek/integration_continue'
            }
        }
        stage('Test') {
            steps {
                bat label: '', script: 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                bat 'mvn deploy'
            }
        }
    }
}