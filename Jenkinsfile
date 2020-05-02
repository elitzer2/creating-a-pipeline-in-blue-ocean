pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''uname -a
exit 1'''
      }
    }

    stage('Deploy for production') {
      when {
        branch 'production'
      }
      steps {
        input 'Finished using the web site? (Click "Proceed" to continue)'
        echo 'Production!!'
      }
    }

  }
  triggers {
    githubPush()
  }
}