pipeline {
    agent any

    stages {
        stage('Cleanup') {
            steps {
                dir ('build') {
                    deleteDir()
                }
                dir ('publish') {
                    deleteDir()
                }
            }
        }
        stage('CMake build') {
            steps {
                cmake arguments: '--preset="release-linux-x64"', installation: 'InSearchPath'
                cmakeBuild buildType: 'Release', buildDir: 'build', installation: 'InSearchPath'
            }
        }
    }
}
