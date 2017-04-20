pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "I am the build"; sleep 3; echo "SUCCESSFULL"'
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Unittests": {
            sh 'echo I am the test; sleep 4'
            
          },
          "System Integration tests": {
            sh 'echo I am another test; sleep 6'
            
          }
        )
      }
    }
    stage('Deploy to DEV') {
      steps {
        sh 'echo Deploying; sleep 6'
      }
    }
    stage('Deploy to INT') {
      steps {
        sh 'echo Deploying to INT'
      }
    }
    stage('Deploy to PRE') {
      steps {
        sh 'echo Deploying to PRE'
      }
    }
    stage('Deploying to PROD') {
      steps {
        sh 'echo Deploying to PROD'
      }
    }
  }
}