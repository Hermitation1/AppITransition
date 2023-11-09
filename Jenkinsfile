pipeline {
    agent {
        docker {
            image 'node:20.9.0-alpine3.18'
            args '-p 3000:3000 --restart=always'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
		sh 'echo "Hello!"'
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
                sh 'sleep 100'
            }
        }
    }
}
