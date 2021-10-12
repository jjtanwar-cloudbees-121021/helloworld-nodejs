pipeline {
  agent none
  stages {
    stage('Test') {
      agent {
        kubernetes {
          yamlFile 'nodjs-pod.yaml'
        }
      }
      steps {
        container('nodejs') {
          echo 'Hello World!'   
          sh 'node --version'
        }
      }
    }
  }
}


