pipeline {
  agent any    

  
  stages {
    stage('Build') {
      steps {
        sh "sudo apt-get update"
        sh "sudo apt install nodejs npm"
        sh "sudo npm install ."
        sh "sudo npm run build"
      }
    }
  }
}
