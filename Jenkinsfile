pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        echo 'Hello'
      }
    }

    stage('Validation') {
      parallel {
        stage('Validation') {
          steps {
            build(propagate: true, job: 'Yashida')
          }
        }

        stage('build') {
          steps {
            build 'one'
          }
        }

      }
    }

    stage('Print') {
      steps {
        echo "${currentBuild.currentResult}"
        echo "${currentBuild.displayName}"
      }
    }

  }
}