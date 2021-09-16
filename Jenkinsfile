pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('build') {
      agent {
        docker {
          image 'node:6-alpine'
        }

      }
      steps {
        sh 'ls'
      }
    }

    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }

  }
}