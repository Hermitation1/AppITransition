pipeline {
  agent {
    docker {
      image 'node:20.9.0-alpine3.18'
      args '-p 3000:3000 -v /var/run/docker.sock:/var/run/docker.sock'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh '''npm install .




'''
      }
    }

    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }

    stage('Deploy') {
      steps {
        sh './jenkins/scripts/deliver.sh'
        sh 'npm install -g serve '
        sh 'serve -s build'
      }
    }

    stage('sleep') {
      steps {
        sleep(unit: 'MINUTES', time: 20)
      }
    }

  }
}