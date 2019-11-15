pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

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
                echo 'Deploying....'
            }
        }
    }
}