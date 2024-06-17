pipeline {
    agent any

    stages {
        stage('CMake build') {
            steps {
                cmake arguments: '--preset="release-linux-x64"', installation: 'InSearchPath'
                cmakeBuild buildType: 'Release', cleanBuild: true, installation: 'InSearchPath', steps: [[withCmake: true]]
            }
        }
    }
}