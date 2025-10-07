pipeline {
    agent {
        dockerfile {
            filename 'Dockerfile'
            label 'jenkins-ubuntu-agent'
            }

    stages {
        stage('S1 - Any Agent') {
            steps {
                sh 'cat /etc/os-release'
                sh 'node -v'
                sh 'npm -v'
            }
        }

        stage('S2 - Ubuntu Agent') {
            steps {
                sh 'cat /etc/os-release'
                sh 'node -v'
                sh 'npm -v'
            }
        }

        stage('S3 - Docker Agent') {
            steps {
                sh 'cat /etc/os-release'
                sh 'node -v'
                sh 'npm -v'
            }
        }
        stage('S4 - Docker File Agent') {
            steps {
                sh 'node -v'
                sh 'npm -v'
                sh 'cowsay -f dragon This is running on docker container'
            }
        }
    }
}
