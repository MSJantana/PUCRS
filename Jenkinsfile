pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'cardapio_online:latest'
    }

    stages {
        stage('Clonar Git') {
            steps {
               git branch: 'main', url: 'https://github.com/MSJantana/PUCRS.git'
            }        
        }
        stage('Construir Imagem Docker - Build') {
            steps {
                script {
                    sh 'docker build -t ${DOCKER_IMAGE} .'
                }
            }
        }
    }       
}