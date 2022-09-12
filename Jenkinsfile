pipeline {
  agent any
  
  parameters {
    choice(name: 'ENVIRONMENT', choices: ['DEV','QAMERGE','UAT','FULLCOPY'], description: 'Select an environment to run tests.' )
  }
  
  stages {
    stage("Init") {
      steps {
        echo 'Init related steps'
      }
    }
    
    stage("Environment") {
      steps {
        echo ${params.ENVIRONMENT}
      }
    }
    
    stage("Automation") {
      when {
        expression { params.ENVIRONMENT == 'UAT' }
      }
      steps {
        echo 'UAT selected' 
      }
    }
    
    stage("End") {
      steps {
        echo 'The end'
      }
    }
  }
}
