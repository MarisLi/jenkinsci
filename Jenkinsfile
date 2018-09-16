pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:6-alpine'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
  }
  environment {
    asd = 'sudo nohup docker daemon -H tcp://0.0.0.0:2375 -H unix:///var/run/docker.sock &'
  }
}