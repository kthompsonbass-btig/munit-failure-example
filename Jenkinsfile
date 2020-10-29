pipeline {
    options {
        buildDiscarder(logRotator(numToKeepStr: '3', artifactNumToKeepStr: '3'))
    }
    // agent any
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2'
            // dockerfile true
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'mvn -B test'
                //sh 'docker pull maven:3.6-jdk-8-alpine'
                //sh 'docker run maven:3.6-jdk-8-alpine mvn -B -X clean test'
            }
        }
    }
}