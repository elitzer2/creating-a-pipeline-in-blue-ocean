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
        sleep 10
        echo 'Production!!'
      }
    }

  }
  triggers {
    githubPush()
  }
}