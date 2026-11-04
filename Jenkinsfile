pipeline {
    agent { docker { image 'python:3.12' } }
    stages {
        stage('Instalar dependencias') {
            steps {
                sh 'pip install --user -r requirements.txt'
            }
        }
    }
}
