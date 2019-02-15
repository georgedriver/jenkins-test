pipeline {
  agent none
  stages {
    stage('Run Parallel Tests') {
      parallel {
        stage('Test On Windows') {
          steps {
            sh 'sleep 10'
          }
        }
        stage('Test On Linux') {
          agent {
            docker {
              image 'busybox'
            }

          }
          steps {
            sh 'sleep 12'
          }
        }
        stage('Test On Mac') {
          steps {
            sh 'sleep 5'
          }
        }
      }
    }
    stage('stage-1') {
      steps {
        sh 'echo "hello"'
      }
    }
  }
  environment {
    EVNEEE = 'value'
  }
}