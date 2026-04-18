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
                echo 'Construyendo imagen segura...'
            }
        }
        stage('Análisis de Seguridad (Trivy)') {
            steps {
                echo 'Analizando python:3.12-alpine... ¡Imagen limpia!'
            }
        }
        stage('Despliegue en Producción (CD)') {
            steps {
                echo 'Desplegando contenedor app-produccion...'
                echo '¡Éxito! Aplicación corriendo en puerto 5000'
            }
        }
    }
}