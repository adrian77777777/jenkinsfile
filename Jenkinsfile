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
                        echo 'Build'
                        sh 'pwd'
                        sh 'make'
                        archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
                           }
                        }
        stage('Test') {
                    steps {
                        sh 'make check || true'
                        junit '**/target/*.xml'
                            }
                       }
        stage('Deploy') {
                    steps {
                        echo 'Deploying....'
                           }
                        }



    }
}