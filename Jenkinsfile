String cron_string "* * * * *"

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
