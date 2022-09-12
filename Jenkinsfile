pipeline {
  agent any
  
  parameters {
    choice(name: 'ENVIRONMENT', choices: ['DEV','QAMERGE','UAT','FULLCOPY'], description: 'Select an environment to run tests.' )
  }
  
  stages {
    stage("Init") {
      echo 'Init related steps'
    }
    
    stage("End") {
      echo 'The end'
    }
  }
}
