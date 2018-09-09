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
    }
    failure{
      echo 'failure...'
    }
  }
}

