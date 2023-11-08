pipeline {
  agent {
    docker {
      image 'node:20.9.0-alpine3.18'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh '''npm install .




'''
        sh 'npm run build'
      }
    }

    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }

    stage('Deliver') {
      steps {
        sh './jenkins/scripts/deliver.sh'
        echo '\'Finished using the web site??? (Click "Proceed" to continue)\''
        sh './jenkins/scripts/kill.sh'
      }
    }

  }
}