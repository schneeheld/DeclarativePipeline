String cron_string "H/2 * * * *"

pipeline {
    agent any
    parameters {
        string(name: 'readonly', defaultValue: 'true', description: 'Read/Write status')
    }
    triggers { cron (cron_string) }
    stages {
        stage('STEP-A') {
            steps {
                echo "${params.readonly}"
            }
        }
    }
}
