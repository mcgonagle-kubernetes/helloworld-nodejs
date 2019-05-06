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
          git url: 'https://github.com/mcgonagle-kubernetes/helloworld-nodejs.git'
          echo 'Hello World!'   
          sh 'node --version'
          sh 'ls'
          sh 'npm run-script helloworld-nodejs/hello.js'
        }
      }
    }
  }
}
