pipeline {
  agent any
  stages {
    stage('maven') {
      parallel {
        stage('maven version') {
          steps {
            sh 'mvn --version'
          }
        }

        stage('run projedct') {
          steps {
            sh 'mvn clean test'
          }
        }

      }
    }

  }
}