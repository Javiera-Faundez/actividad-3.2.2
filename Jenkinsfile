pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Instalar dependencias') {
            steps {
                sh 'python3 -m venv venv'
                sh '. venv/bin/activate && pip install -r requirements.txt'
            }
        }
        stage('OWASP Dependency-Check') {
            steps {
                dependencyCheck additionalArguments: '--scan ./ --format HTML --format XML --prettyPrint',
                                odcInstallation: 'dependency-check'
                dependencyCheckPublisher pattern: '**/dependency-check-report.xml'
            }
        }
    }
}
