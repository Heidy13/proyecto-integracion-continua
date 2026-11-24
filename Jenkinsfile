pipeline {
    agent any

    stages {
        stage('Obtener codigo') {
            steps {
                checkout scm
            }
        }
        stage('Verificar estructura') {
            steps {
                sh 'ls -la'
                sh 'test -f Dockerfile'
                sh 'test -f docker-compose.yml'
                sh 'test -f composer.json'
            }
        }
        stage('Informacion del entorno') {
            steps {
                sh 'java -version'
                sh 'git --version'
            }
        }
    }
}
