pipeline {
  agent any
  stages {
     
    stage('Build') {
      steps {
        nodejs(nodeJSInstallationName: 'Node 6.x', configId: '<config-file-provider-id>') {
        sh 'npm install'
        sh 'npm install -g serve'
      }
      }
    }
            
    stage('Test') {
      steps {
        nodejs(nodeJSInstallationName: 'Node 6.x', configId: '<config-file-provider-id>') {
        sh 'npm test'
      }
      }
    }
    stage('Deploy') {
        steps {
            sh 'serve -s build'
        }
    } 
  }
}
