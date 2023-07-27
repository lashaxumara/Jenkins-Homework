pipeline {
  agent any
  stages {
    stage('maven') {
      parallel {
        stage('mvn version') {
          steps {
            script {
              def mvnHome = tool 'Maven 3.9.3'
              bat "${mvnHome}\\bin\\mvn --version"
            }

          }
        }

        stage('compile mvn project') {
          steps {
            script {
              def mvnHome = tool 'Maven 3.9.3'
              bat "${mvnHome}\\bin\\mvn clean test"
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