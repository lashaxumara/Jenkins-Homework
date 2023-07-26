pipeline {
  agent any
  stages {
    stage('check Mvn version') {
      parallel {
        stage('check Mvn version') {
          steps {
            sh '''pipeline {
    agent any
    stages {
        stage(\'Check Maven Version\') {
            steps {
                bat \'mvn --version\'
            }
        }
      
    }
}
'''
            }
          }

          stage('Run mvn project') {
            steps {
              sh '''pipeline {
    agent any
    stages {
        stage(\'Check Maven Version\') {
            steps {
                bat \'mvn clean package\'
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