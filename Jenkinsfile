pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        build 'PES1UG21CS562-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage ('Test') {
      steps {
        sh './output'
      }
    }
    stage ('Deploy') {
      steps {
        echoo 'deploy'
      }
    }
  }
  post {
    failure {
      error 'Pipeline Failed'
    }
  }
}
