#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                script {
                    echo "Building the application..."
                }
            }
        }
        stage('test') {
            steps {
                script {
                    echo "Testing the application..."
                }
            }
        }
        stage('deploy') {
            steps {
                script {
                    def dockerCmd = "docker run -p 8080:80 -d dannyboy01/my-app:dev"
                    sshagent(['ssh-key']) {
                        sh "scp docker-compose.yml ubuntu@100.25.153.24:/home/ubuntu"
                        sh "ssh -o StrictHostKeyChecking=no ubuntu@100.25.153.24 ${dockerCmd}"
                    }
                }
            }
        }
    }
}
