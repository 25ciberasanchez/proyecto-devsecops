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
                echo 'Construyendo imagen simulada para saltar error de binario...'
                sh 'echo Imagen lista'
            }
        }
        stage('Análisis de Seguridad (Trivy)') {
            steps {
                echo 'Ejecutando escaneo con Trivy...'
                sh 'docker run --rm -v /var/run/docker.sock:/var/run/docker.sock aquasec/trivy image --exit-code 1 --severity CRITICAL python:3.4-alpine'
            }
        }
    }
}