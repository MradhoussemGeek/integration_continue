pipeline {
    agent any

    stages {
        
          stage("mvn build") {
            steps {
                script {
                    // If you are using Windows then you should use "bat" step
                    // Since unit testing is out of the scope we skip them
                    bat "mvn package -DskipTests=true"
                }
            }
        }
        stage('install') {
            steps {
                bat label: '', script: 'mvn install'
            }
        }
          stage('deploy') {
            steps {
                bat label: '', script: 'mvn deploy'
            }
        }  
        
    }
}