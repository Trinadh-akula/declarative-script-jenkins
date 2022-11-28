pipeline {
  agent any
  environment {
    myenv1="dev"
  }
  parameters {
  string defaultValue: 'dev', description: 'pt', name: 'platform', trim: false
  choice choices: ['linux', 'hp-ux', 'solaris', 'centos', 'red-hat'], description: 'select any one', name: 'ostype'
}

  stages {
    stage('working with variables') {
      steps {
        script {
          def myval1=20
          println "myval1 value is ${myval1}"
          println "myenv1 environment is ${env.myenv1}"
          //printing global variables
          println "Printing build id ${env.BUILD_ID}"
          // printing parameters values
          println "my environment parameter is ${params.platform}"
          println "my selected ostype is ${params.ostype}"
        }
      }
    }
  }
}
