pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''uname -a
date'''
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