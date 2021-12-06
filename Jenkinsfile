pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        echo 'building'
      }
    }

    stage('testing') {
      parallel {
        stage('testing') {
          steps {
            echo 'testing'
          }
        }

        stage('performancetesting') {
          steps {
            sh ' cat index.html'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }

  }
}