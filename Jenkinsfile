pipeline {
  agent {
    docker {
      image 'node:16.14.0-alpine'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh '''pwd &&
ls &&
npm -v &&
npm config set registry https://registry.npmmirror.com && npm install &&
node -v '''
      }
    }

  }
  environment {
    CI = 'true'
  }
}