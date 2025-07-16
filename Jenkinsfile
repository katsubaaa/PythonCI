pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/example/ci-demo.git'
      }
    }
    stage('Install') {
      steps {
        sh 'pip install -r requirements.txt'
      }
    }
    stage('Test') {
      steps {
        sh 'pytest'
      }
    }
  }
}
