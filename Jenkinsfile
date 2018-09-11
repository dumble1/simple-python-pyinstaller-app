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
      slackSend channel: '#test_jenkins', color: 'good', message: 'Hei Moi Treve!!Success!!!'
    }
    failure{
      echo 'failure...'
      slackSend channel: '#test_jenkins', color: 'warning', message: 'hej hej Failure...'
    }
  }
}

