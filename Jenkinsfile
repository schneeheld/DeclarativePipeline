pipeline {
    agent any
    parameters {
        string(name: 'readonly', defaultValue: 'true', description: 'Read/Write status')
    }
    stages {
        stage('STEP-A') {
            steps {
                echo "${params.readonly}"
            }
        }
    }
}
