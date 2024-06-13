pipeline {
    agent any

    stages {
        stage('Configure') {
            steps {
                sh '''
                    cmake -S . -B build --preset="release-linux-x64"
                '''
            }
        }
        stage('Build') {
            steps {
                sh '''
                   cmake --build build
                '''
            }
        }
    }
}