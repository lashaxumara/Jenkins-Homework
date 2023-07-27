pipeline {
  agent any
  stages {
    stage('maven') {
      parallel {
        stage('mvn version') {
          steps {
            powershell(script: 'mvn --version', returnStatus: true)
          }
        }

        stage('compile mvn project') {
          steps {
            powershell(script: 'mvn compile', returnStatus: true)
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
