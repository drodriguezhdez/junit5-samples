pipeline {
    /*agent {
        label 'worker'
    }*/
    agent any
    /*triggers {
        cron('* * * * *')
    }*/

    environment {
        DD_SERVICE_NAME = 'junit5-samples'
        DD_API_KEY = credentials('dd-api-key')
        DD_INTEGRATION_JUNIT_ENABLED = true
    }

    stages {
        stage("junit5-migration-gradle") {
            steps {
              dir("junit5-migration-gradle") {
                sh "./gradlew test"
              }
            }
        }
    }
}
