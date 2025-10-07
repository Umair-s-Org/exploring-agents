pipeline {
    agent {
        dockerfile { 
            filename 'Dockerfile'
            label 'jenkins-ubuntu-agent'
        }
    }
    stages {
        stage('Stage-1') {
            steps {
                echo "Generating a random file"
                sh 'echo $((RANDOM)) > /tmp/imp-file-$BUILD_ID'
                sh 'ls -l /tmp/imp-file-$BUILD_ID'
                sh 'cat /tmp/imp-file-$BUILD_ID'
            }
        }
        stage('Stage-2') {
            steps {
                echo "Reading the same file in Stage-2"
                sh 'ls -l /tmp/imp-file-$BUILD_ID'
                sh 'cat /tmp/imp-file-$BUILD_ID'
            }
        }
        stage('Stage-3') {
            steps {
                echo "Verifying file in Stage-3"
                sh 'cat /tmp/imp-file-$BUILD_ID'
            }
        }
        stage('Stage-4') {
            steps {
                echo "Inspecting before exit"
                sh 'ls -l /tmp/imp-file-$BUILD_ID'
                sh 'cat /tmp/imp-file-$BUILD_ID'
                echo "Sleeping to keep container alive"
                sh 'sleep 120s'
            }
        }
    }
}
