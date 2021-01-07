pipeline {
  agent any
  stages {
     
    stage('Build') {
      steps {
        sh 'npm install'
        sh 'npm install -g serve'
      }
    }
            
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Deploy') {
        steps {
            sh 'serve -s build'
        }
    } 
  }
}
