pipeline {
  agent {
    docker {
      image 'node:16.14.0-alpine'
    }

  }
  stages {
    stage('Build') {
      steps {
        git(url: 'https://ghproxy.fsofso.com/https://github.com/uyoungco/simple-node-js-react-npm-app.git', changelog: true)
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