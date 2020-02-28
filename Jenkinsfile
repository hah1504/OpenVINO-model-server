pipeline {
  agent {
    docker {
      image 'clearlinux'
    }

  }
  stages {
    stage('test') {
      steps {
        sh 'echo "Hello from docker" && ls -la'
      }
    }

  }
}