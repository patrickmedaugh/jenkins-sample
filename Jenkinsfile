pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('build') {
            steps {
                sh 'npm build'
            }
        },
        stage('test') {
            steps {
                retry(3) {
                    sh 'npm test'
                }
            }
        }
    }
}
