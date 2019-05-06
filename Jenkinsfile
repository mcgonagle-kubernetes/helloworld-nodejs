pipeline {
  agent { label 'nodejs-app' }
    stages {
      stage('Build') {
        steps {
            container('nodejs') {
                echo 'Building...'
                sh 'npm install'
            }
            }
        }
      stage('Test') {
      steps {
        sh 'java -version'
        container('nodejs') {
          echo 'Hello World!'   
          sh 'node --version'
          sh 'npm test'
        }
      }
    }
  }
}
