pipeline {
  agent any
  stages {
    stage('Build') {
      options { timestamps() }
      steps {
        echo 'Building...'
        echo 'build: ${env.BUILD_ID} on ${env.JENKINS_URL}'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing....'
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
      options { timestamps() }
      steps {
        echo 'Deploying....'
      }
    }
    stage('Prod') {
      steps {
        sh 'echo "Production..."'
        sleep 10
      }
    }
  }
}
