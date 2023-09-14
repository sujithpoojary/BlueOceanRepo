pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        echo 'Hello'
      }
    }

    stage('Validation') {
      steps {
        build(propagate: true, job: 'Yashida')
      }
    }

  }
}