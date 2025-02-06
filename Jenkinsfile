pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
                sh '''
                    java -jar target/jekins-practice-0.0.1-SNAPSHOT.jar
                '''
            }
        }
    }
}