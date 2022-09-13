pipeline {
  agent any
  
  parameters {
    choice(name: 'ENVIRONMENT', choices: ['DEV','QAMERGE','UAT','FULLCOPY'], description: 'Select an environment to run tests.' )
    booleanParam(name: 'performQAValidation', defaultValue: true, description: 'Perform QA validation?')
  }
  
  stages {
    stage("Init") {
      steps {
        echo 'Init related steps'
      }
    }
    
    stage("Environment") {
      steps {
        echo "${params.ENVIRONMENT}"
      }
    }
    
    stage("UAT") {
      when {
        expression { params.ENVIRONMENT == 'UAT' }
      }
      steps {
        echo 'UAT selected' 
      }
    }
    
    stage("Automation") {
      when {
        expression { params.performQAValidation == true }
      }
      steps {
        echo 'Performing automation tests' 
      }
    }
    
    stage("End") {
      steps {
        echo 'The end'
      }
    }
  }
}
