pipeline {
  agent {
    
    docker {
      image 'cypress/base:10'
    }
  }

  stages {
    stage('build and test') {
      environment {
       
        CYPRESS_RECORD_KEY = credentials('4204fd91-e25b-4f77-ba18-4284e56f7c14')
      }

      steps {
        sh 'npm ci'
        sh "npm run test:ci:record"
      }
    }
  }
}
