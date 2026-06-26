pipeline {
    agent any

        environment {
           APP_NAME = 'Docker Demo'
       }

    stages {

        stage('Stop Containers') {
            steps {
                sh '/usr/local/bin/docker compose down || true'
            }
        }

        stage('Build and Start Containers') {
            steps {
                echo "Application: ${APP_NAME}"        
                sh '/usr/local/bin/docker compose up -d --build'
            }

        }

    }
}
