pipeline {
  agent any

  stages {
    stage('maven') {
      parallel {
        stage('mvn version') {
          steps {
            script {
              def mvnHome = tool 'Maven 3.9.3'
              sh "${mvnHome}/bin/mvn --version"
            }
          }
        }

        stage('compile mvn project') {
          steps {
            script {
              def mvnHome = tool 'Maven 3.9.3'
              sh "${mvnHome}/bin/mvn compile"
            }
          }
        }
      }
    }

    stage('End') {
      steps {
        echo 'The end...'
      }
    }
  }
}
