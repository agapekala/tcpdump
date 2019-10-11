pipeline {
  agent any
  stages {
    stage('Build') {
      agent {
        docker {
          args '-u 0'
          image 'ubuntu'
        }

      }
      steps {
        sh '''apt update
'''
        sh 'apt install gcc make libpcap-dev'
        sh './configure && make'
      }
    }
  }
}