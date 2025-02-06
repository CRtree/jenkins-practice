pipeline {
    agent {
        label 'docker'
    }
    stages {
        stage('Docker node test') {
              agent {
                docker {
                  // Set both label and image
                  label 'docker'
                  image 'node:22.13.1-alpine3.21'
                }
              }
              steps {
                sh 'node --version'
              }
        }
        stage('Test') {
            steps {
                sh 'node --eval "console.log(process.arch,process.platform)"'
            }
        }
    }
}