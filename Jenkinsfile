pipeline {
  agent any
    
  stages {
     
    stage('Build') {
      steps {
        sh 'npx serve -s build'
      }
    }
            
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Deploy') {
        steps {
            sh 'npx serve -s build'
        }
    } 
  }
}
