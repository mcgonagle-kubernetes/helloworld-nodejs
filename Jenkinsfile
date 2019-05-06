pipeline {
  agent { label 'nodejs-app' }
  stages {
    stages {
      stage('Build') {
            container('nodejs') {
                echo 'Building...'
                sh 'npm install'
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
