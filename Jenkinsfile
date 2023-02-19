pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES1UG20CS136 PES1UG20CS136.cpp'
        build job: 'PES1UG20CS136-1'
        echo 'Build stage successful'
      }
    }
    stage('Test') {
      steps {
        sh './PES1UG20CS136'
        echo 'Test stage successful'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment stage'
        ls '1234' 
      }
    }
  }
  post {
    failure {
      echo 'Pipline failed'
    }
  }
}
