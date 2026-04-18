pipeline {
    agent any
    stages {
        stage('Descargar Código') {
            steps {
                git branch: 'desarrollo', url: 'https://github.com/25ciberasanchez/proyecto-devsecops.git'
            }
        }
        stage('Construir Imagen (Build)') {
            steps {
                echo 'Construyendo imagen simulada...'
            }
        }
        stage('Análisis de Seguridad (Trivy)') {
            steps {
                echo 'Buscando vulnerabilidades CRÍTICAS en python:3.4-alpine...'
                echo 'FALLO: Se han detectado 45 vulnerabilidades CRÍTICAS (CVE-2023-XXXX)'
                sh 'exit 1'
            }
        }
    }
}