String cron_string_true = "* * * * *"
String cron_string_false = "H/3 * * * *"

pipeline {
    agent any
    parameters {
        string(name: 'readonly', defaultValue: 'true', description: 'Read/Write status')
    }
    triggers { cron ( '${params.readonly}' == "true" ? cron_string_true : cron_string_false) }
    stages {
        stage('STEP-A') {
            steps {
                echo "${params.readonly}"
            }
        }
    }
}
