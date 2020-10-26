pipeline {
    options {
        buildDiscarder(logRotator(numToKeepStr: '3', artifactNumToKeepStr: '3'))
    }
    agent {
        dockerfile true
    }
    stages {
        stage('Test') {
            steps {
                sh 'mvn -B -X clean test'
            }
        }
    }
}