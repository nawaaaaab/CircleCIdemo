pipeline {
  agent any
  stages {
    stage('Testing') {
      steps {
        echo 'Testing...'
        sh 'flake8 --exclude=venv* --statistics'
        sh 'pytest -v --cov=calculator'
      }
    }

  }
}