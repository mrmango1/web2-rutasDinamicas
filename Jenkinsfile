pipeline {
    agent any

    stages {
        stage('Instalación de Dependencias') {
            steps {
                sh 'npm install'
            }
        }

        stage('Construyendo la App') {
            steps {
                sh 'npm run ng build'
            }
        }

        stage('Moviendo la carpeta para su ejecución') {
            steps {
                sh 'cp -r $WORKSPACE/dist $HOME/Work/itsmqet/nginx'
            }
        }
    }
}
