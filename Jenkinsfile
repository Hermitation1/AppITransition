pipeline {
  agent any
   
  stages {
    stage('Build') {
      agent {
        docker { 
          image 'ununtu:18.04'
          reuseNode true
        }
      }
      steps {
        sh "apt-get update"
        sh "apt install nodejs npm"
        sh "npm install ."
        sh "npm run build"
      }
    }
  }
}
