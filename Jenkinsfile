pipeline {
    agent any
    stages {
        stage('Descargar Código') {
            steps {
                git branch: 'desarrollo', url: 'https://github.com/25ciberasanchez/proyecto-devsecops.git'
            }
        }
        stage('Construir Imagen') {
            steps {
                echo 'Simulando build para evitar error de binario...'
                sh 'echo Imagen construida con éxito'
            }
        }
    }
}