pipeline {
    agent any

    tools {
        maven 'Maven3'
        jdk 'jdk-17'
    }

    environment {
        SONAR_HOST_URL = 'http://localhost:9000'
        ARTIFACTORY_URL = 'http://localhost:8081/artifactory'
        ARTIFACTORY_REPO = 'monolito'
        ARTIFACTORY_CREDS = 'ARTIFACTORY_CREDENTIALS'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }
    }
}
