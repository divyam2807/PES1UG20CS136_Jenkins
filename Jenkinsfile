pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES1UG20CS136_Divyam PES1UG20CS136_Divyam.cpp'
        build job: 'PES1UG20CS136-1'
        echo 'Build stage successful'
      }
    }
    stage('Test') {
      steps {
        sh './PES1UG20CS136_Divyam'
        echo 'Test stage successful'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment stage'
        //sh 'exit 1' //uncomment this for error part
      }
    }
  }
  post {
    failure {
      echo 'Pipline failed'
    }
  }
}
