pipeline {
    agent any
    stages {
        stage('Descargar Código') {
            steps {
                git branch: 'desarrollo', url: 'https://github.com/25ciberasanchez/proyecto-devsecops.git'
            }
        }
        stage('Construir Imagen Docker (Build)') {
            steps {
                sh 'docker build -t mi-app-segura:latest .'
            }
        }
    }
}