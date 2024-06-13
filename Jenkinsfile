pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                    cmake build . --out-dir "build" --preset="release-linux-x64"
                '''
            }
        }
    }
}