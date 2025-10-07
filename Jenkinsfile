pipeline {
    agent any

    stages {
        stage('S1 - Any Agent') {
            steps {
                sh 'cat /etc/os-release'
                sh 'node -v'
                sh 'npm -v'
            }
        }

        stage('S2 - Ubuntu Agent') {
            agent { label 'jenkins-ubuntu-agent' }
            steps {
                sh 'cat /etc/os-release'
                sh 'node -v'
                sh 'npm -v'
            }
        }

        stage('S3 - Docker Agent') {
            agent {
                docker {
                    // alwaysPull true
                    image 'node:18-alpine'
                    label 'jenkins-ubuntu-agent'
                }
            }
            steps {
                sh 'cat /etc/os-release'
                sh 'node -v'
                sh 'npm -v'
            }
        }
        stage('S4 - Docker File Agent') {
            agent {
                docker {
                    // alwaysPull true
                    image 'node:18-alpine'
                    label 'jenkins-ubuntu-agent'
                }
            }
            steps {
                sh 'node -v'
                sh 'npm -v'
                sh 'cowsay -f dragon This is running on docker container'
            }
        }
    }
}
