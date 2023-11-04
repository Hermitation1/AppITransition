pipeline {
  agent {
    docker { image 'ununtu:18.04' }
  }  
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
