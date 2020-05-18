pipeline {
  agent any
  stages {
    stage('Testing') {
      steps {
        ws(dir: 'hello')
      }
    }

    stage('Deploy') {
      agent any
      steps {
        echo 'Done'
      }
    }

  }
}