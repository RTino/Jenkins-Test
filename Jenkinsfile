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
          "Test": {
            sh 'echo I am the test; sleep 4'
            
          },
          "Test2": {
            sh 'echo I am another test; sleep 6'
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo Deploying; sleep 6'
      }
    }
  }
}