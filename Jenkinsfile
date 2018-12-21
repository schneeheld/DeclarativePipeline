pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        echo 'build: ${env.BUILD_ID} on ${env.JENKINS_URL}'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing...'
          }
        }
        stage('Functional') {
          steps {
            sh 'echo "Functional tests..."'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}