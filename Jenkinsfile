pipeline {
  agent any    

  
  stages {
    stage('Build') {
      steps {
        sh "apt-get update"
        sh "apt install nodejs npm"
        sh "npm install ."
        sh "npm run build"
      }
    }
  }
}
