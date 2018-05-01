pipeline {
    agent {
    label 'jdk8'
  }
    stages {
        stage('Testing') {
        parallel {
          stage('Java 7') {
            agent { label 'jdk7' }
            steps {
              container('maven') {
                sh 'mvn -v'
              }
            }
          }
          stage('Java 8') {
            agent { label 'jdk8' }
            steps {
              container('maven') {
                sh 'mvn -v'
              }
            }
          }
        }
      }
    }
}
