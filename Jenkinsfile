pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh './test.sh'
      }
    }
  }
  post{
    success{
      echo 'Success!'
      slackSend channel: '#test_jenkins', color: 'good', message: 'Success!!!'
    }
    failure{
      echo 'failure...'
      slackSend channel: '#test_jenkins', color: 'warning', message: 'Failure...'
    }
  }
}

