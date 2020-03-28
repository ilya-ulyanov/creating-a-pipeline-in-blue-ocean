pipeline {
  agent {
    docker {
      image 'node:13-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        sh './jenkins/scrips/test.sh'
      }
    }

  }
  environment {
    CI = 'true'
  }
}