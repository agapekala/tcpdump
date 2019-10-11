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
        sh 'apk get gcc libc-dev openssl-dev make libpcap-dev'
      }
    }
  }
}