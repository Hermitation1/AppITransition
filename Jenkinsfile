pipeline {
  agent any

  
  stages {
    stage('Build') {
      steps {
        apt update
        sudo apt install nodejs npm
        npm install .
        npm run build
      }
    }
  }
}
