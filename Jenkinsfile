pipeline {
  agent any
  stages {
    stage('Build') {
      agent {
        docker {
          args '-u 0'
          image 'alpine'
        }

      }
      steps {
        sh 'apk add make gcc openssl-dev libc-dev libpcap-dev'
        sh './configure && make'
      }
    }
  }
}