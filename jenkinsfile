pipeline {
  agent any

  parameters {
    string(name: 'NAME', description: 'Please tell me your name?')
    string(name: 'Address', description: 'Enter your address, for the pipeline trigger')
    text(name: 'DESC', description: 'Describe about the job details')
    choice(name: 'BRANCH', choices: ['Dev', 'Stage', 'prod', 'uat'], description: 'Choose one environment')
    booleanParam(name: 'SKIP_TEST', defaultValue: false, description: 'Skip running test cases?')
    password(name: 'SONAR_SERVER_PWD', defaultValue: '', description: 'Enter Sonar server password')
  }

  stages {
    stage('Printing Parameters') {
      steps {
        echo "Hello ${params.NAME}"
        echo "Address: ${params.Address}"
        echo "Job Details: ${params.DESC}"
        echo "Skip Running Test case?: ${params.SKIP_TEST}"
        echo "Branch Choice: ${params.BRANCH}"
        echo "APP Password: ${params.SONAR_SERVER_PWD}"
      }
    }
  }
}
