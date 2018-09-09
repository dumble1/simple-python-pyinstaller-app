pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        bash './test.sh'
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

