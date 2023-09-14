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
     
    stage('Print') {
      steps {
        echo currentBuild.result
        echo currentBuild.displayName
     }
    }
  }
}
