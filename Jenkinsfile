pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/rojakurva/cwa-server.git', branch: 'master')
      }
    }

    stage('compile') {
      steps {
        bat 'mvn clean compile'
      }
    }

  }
}