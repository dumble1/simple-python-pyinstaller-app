pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh './test.sh'
        echo 'yksi kaksi kolme nelja viisi kuusi seitseman kahdeksan yhdeksan kymmenen'
      }
    }
  }
  post{
    success{
      echo 'Success!'
      slackSend channel: '#test_jenkins', color: 'good', message: 'yksi Hei Moi Treve!!Success!!!'
    }
    failure{
      echo 'failure...'
      slackSend channel: '#test_jenkins', color: 'warning', message: 'hej hej Failure...'
    }
  }
}

