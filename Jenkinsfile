pipeline {
    agent any
    parameters {
        string(name: 'readonly', defaultValue: 'true', description: 'Read/Write status')
    }
    triggers { cron ('H/2 * * * *') }
    stages {
        stage('STEP-A') {
            steps {
                echo "${params.readonly}"
            }
        }
    }
}
