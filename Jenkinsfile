pipeline {
    agent any

    stages {
        stage('Configure') {
            steps {
                dir('build') {
                    sh 'cmake ../'
                }
            }
        }
        stage('Build') {
            steps {
                dir('build') {
                    sh 'cmake --build .'
                }
            }
        }
    }
}