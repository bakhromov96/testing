pipeline {
  agent any
  stages {
    stage('Testing') {
      steps {
        mail(subject: 'Testing', body: 'It started testing', from: 'Jenkins Error Check', to: 'bakhromovkhurshid@gmail.com')
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