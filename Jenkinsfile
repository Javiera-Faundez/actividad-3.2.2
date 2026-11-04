pipeline {
    agent {
        docker { image: 'python:3.11-slim' }
    }
    stages {
        stage('Setup') {
            steps {
                sh 'python3 -m venv venv'
            }
        }
    }
}
