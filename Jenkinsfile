pipeline {
  agent {
    label 'amazon-linux'
  }
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
        sleep(time: 10, unit: 'MINUTES')
        echo 'Production!!'
      }
    }

  }
  triggers {
    githubPush()
  }
}
