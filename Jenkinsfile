pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'uname -a'
      }
    }
    stage('Deploy for production') {
        when {
            branch 'production'
        }
        steps {
            input message: 'Finished using the web site? (Click "Proceed" to continue)'
            echo 'Production!!'
        }
    }
  }
}
