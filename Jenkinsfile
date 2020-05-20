pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/rojakurva/cwa-server.git', branch: 'master')
      }
    }

    stage('compile') {
      parallel {
        stage('compile') {
          steps {
            bat 'mvn clean compile'
          }
        }

        stage('install') {
          steps {
            bat 'mvn install'
          }
        }

      }
    }

  }
}