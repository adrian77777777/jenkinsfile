pipeline {
    agent any
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!'
                  }
                         }
        stage('Build') {
                    steps {
                        sh 'make'
                        archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
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