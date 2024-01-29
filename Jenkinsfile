pipeline {
    agent any

    stages {
        stage('Instalación de Dependencias') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }

        stage('Construyendo la App') {
            steps {
                script {
                    sh 'npm run ng build'
                }
            }
        }

        stage('Moviendo la carpeta para su ejecución') {
            steps {
                script {
                    sh 'cp -r /Users/mrmango1/.jenkins/workspace/web2-rutasDinamicas/dist /Users/mrmango1/Work/itsmqet/nginx'
                }
            }
        }
    }
}
