pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git branch: 'main', url: 'https://github.com/katsubaaa/PythonCI'
      }
    }
    stage('Install') {
      steps {
        sh '''
          python3 -m venv venv
          . venv/bin/activate
          pip install --upgrade pip
          pip install -r requirements.txt
        '''
      }
    }
    stage('Test') {
      steps {
        sh '''
          . venv/bin/activate
          pytest
        '''
      }
    }
  }
}
