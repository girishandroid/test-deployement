node {
    env.NODEJS_HOME = "${tool 'node'}"
    // on linux / mac
    env.PATH="${env.NODEJS_HOME}/bin:${env.PATH}"
    // on windows
    // env.PATH="${env.NODEJS_HOME};${env.PATH}"
    echo env.PATH;
    
//withNPM(npmrcConfig: 'e4f5f15c-7dbc-4b6d-b98e-465c6c4e492d') {
        //sh '/Users/shirishakhare/.jenkins/tools/jenkins.plugins.nodejs.tools.NodeJSInstallation/node/bin/node --version'
        sh 'npm --version'
  //  }
}
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
