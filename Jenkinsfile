pipeline {
  agent any
  stages {
    stage('check Mvn version') {
      parallel {
        stage('check Mvn version') {
          steps {
            sh 'mvn --version'
          }
        }

        stage('Run mvn project') {
          steps {
            sh '''pipeline {
    agent any
    stages {
        stage(\'Build\') {
            steps {
                sh \'mvn clean package\'
            }
        }
  
    }
}
'''
            }
          }

        }
      }

    }
  }