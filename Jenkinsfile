pipeline {
    agent { docker { image 'python:3.12' } }
    stage('Instalar dependencias') {
        steps {
            sh 'apt-get update && apt-get install -y python3 python3-venv'
            sh 'python3 -m venv venv'
            
        }
    }
}
