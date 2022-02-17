pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Installing Dependencies ...'
        sh 'python3 -m venv venv ; . venv/bin/activate ; pip install -r requirements.txt'
        echo 'Running Linter'
        sh 'flake8 --exclude=venv* --statistics'
        echo 'Running Unit Test Cases'
        sh 'pytest -v --cov=calculator'
      }
    }

  }
}