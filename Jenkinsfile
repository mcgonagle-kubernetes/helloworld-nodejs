pipeline {
  agent { label 'nodejs-app' }
    stages {
      stage('Build') {
        steps {
            container('nodejs') {
                echo 'Building...'
            }
          }
        }
      stage('Test') {
      steps {
        container('nodejs') {
           echo 'Testing...'
        }
      }
    }
    stage('Deploy') {
      steps {
          container('nodejs') {
           echo 'Deploying...'
          }
        }
      }
  }
}

