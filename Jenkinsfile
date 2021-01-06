pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Git') {
      steps {
        git 'https://github.com/girishandroid/test-deployement.git'
      }
    }
     
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
  }
     
    stage('Deploy') {
        steps {
            sh 'npx serve -s build'
        }
    }  
}