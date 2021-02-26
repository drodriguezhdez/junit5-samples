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
        stage("junit5-jupiter-extensions") {
            steps {
                sh "cd junit5-jupiter-extensions && ./gradlew test'"
            }
        }
    }
}
