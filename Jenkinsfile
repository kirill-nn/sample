pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                    cmake build . --preset="release-linux-x64"
                '''
            }
        }
    }
}