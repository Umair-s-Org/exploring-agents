pipeline {
    agent {
        dockerfile {
            filename 'Dockerfile'
            label 'jenkins-ubuntu-agent'
            }
        }

    stages {
        stage('S1') {
            steps {
                sh 'cat /etc/os-release'
                sh 'node -v'
                sh 'npm -v'
            }
        }

        stage('S2') {
            steps {
                sh 'cat /etc/os-release'
                sh 'node -v'
                sh 'npm -v'
            }
        }

        stage('S3') {
            steps {
                sh 'cat /etc/os-release'
                sh 'node -v'
                sh 'npm -v'
            }
        }
        stage('S4') {
            steps {
                sh 'node -v'
                sh 'npm -v'
                sh 'cowsay -f dragon This is running on docker container'
            }
        }
    }
}
