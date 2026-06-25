pipeline {
    agent any

    stages {

        stage('Stop Containers') {
            steps {
                sh '/usr/local/bin/docker compose down || true'
            }
        }

        stage('Build and Start Containers') {
            steps {
                sh '/usr/local/bin/docker compose up -d --build'
            }
        }

    }
}
